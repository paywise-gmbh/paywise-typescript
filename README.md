# paywise TypeScript SDK

[![npm](https://img.shields.io/npm/v/@paywise/sdk)](https://www.npmjs.com/package/@paywise/sdk)

Official TypeScript/JavaScript client for the paywise **Case Management API v2** and **Partner API v2**.

- API documentation: https://docs.paywise.de
- Specs and SDK configuration: [paywise-gmbh/developer-resources](https://github.com/paywise-gmbh/developer-resources)

> This SDK is generated with [Fern](https://buildwithfern.com) from the published OpenAPI specs. Please open issues and pull requests in [developer-resources](https://github.com/paywise-gmbh/developer-resources), not against the generated code here.

## Installation

```sh
npm install @paywise/sdk
```

Requires Node.js 18 or newer. The package has no runtime dependencies.

## Usage

```ts
import { PaywiseClient, PaywiseEnvironment } from "@paywise/sdk";

const client = new PaywiseClient({
  environment: PaywiseEnvironment.Sandbox, // or PaywiseEnvironment.Production
  token: process.env.PAYWISE_API_KEY,
});

const health = await client.caseManagement.health.check();
```

Both APIs share one client:

- `client.caseManagement.*` — claims, orders, mandates, debtors, payments, statements, webhooks, …
- `client.partner.*` — managed companies, company users, usage, webhooks, …

### Acting on behalf of a company (Partner keys)

Partner keys call the Case Management API for a managed company by sending `X-On-Behalf-Of-Company`. Set it once on the client:

```ts
const companyClient = new PaywiseClient({
  environment: PaywiseEnvironment.Sandbox,
  token: process.env.PAYWISE_PARTNER_API_KEY,
  onBehalfOfCompany: "<company id>",
});
```

Direct Case Management keys must not send this header.

### Pagination

List methods return a page that can be iterated across all pages:

```ts
const claims = await client.caseManagement.claims.listClaims({ limit: 50 });
for await (const claim of claims) {
  console.log(claim.id);
}
```

### Errors

Non-2xx responses throw a typed error per status code (for example `Paywise.caseManagement.UnauthorizedError`), all extending `PaywiseError`:

```ts
import { PaywiseError } from "@paywise/sdk";

try {
  await client.caseManagement.claims.listClaims();
} catch (err) {
  if (err instanceof PaywiseError) {
    console.log(err.statusCode, err.body);
  }
}
```

### Retries and idempotency

Failed requests (408, 429, 5xx) are retried twice by default (`maxRetries` on the client or per request). Write operations that accept an `Idempotency-Key` take it as a request parameter, and retries reuse the same key.

## Reference

The full list of methods is in [reference.md](./reference.md).

## License

MIT — see [LICENSE](./LICENSE).
