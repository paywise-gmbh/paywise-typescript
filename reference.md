# Reference

## Claims

<details><summary><code>client.caseManagement.claims.<a href="/src/api/resources/caseManagement/resources/claims/client/Client.ts">listClaims</a>({ ...params }) -> core.Page&lt;Paywise.Claim, Paywise.PaginatedClaimList&gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Claims addressed by their stable UUID and current relationships.

Read claims throughout their lifecycle using URLs that remain valid after
internal order moves. Standalone creation requires a draft `order_id`;
the relationship is read-only thereafter. Create, PATCH, and DELETE require
a draft order and otherwise return `409 claim_not_editable`. An expired
draft instead returns `409 order_expired`. Tenant-scoped by the
authenticated company.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse = await client.caseManagement.claims.listClaims();
for await (const item of pageableResponse) {
  console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.caseManagement.claims.listClaims();
while (page.hasNextPage()) {
  page = await page.getNextPage();
}

// You can also access the underlying response
const response = page.response;
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.ListClaimsRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ClaimsClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.claims.<a href="/src/api/resources/caseManagement/resources/claims/client/Client.ts">createClaim</a>({ ...params }) -> Paywise.Claim</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Claims addressed by their stable UUID and current relationships.

Read claims throughout their lifecycle using URLs that remain valid after
internal order moves. Standalone creation requires a draft `order_id`;
the relationship is read-only thereafter. Create, PATCH, and DELETE require
a draft order and otherwise return `409 claim_not_editable`. An expired
draft instead returns `409 order_expired`. Tenant-scoped by the
authenticated company.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.claims.createClaim({
  'Idempotency-Key': 'Idempotency-Key',
  body: {
    type: 'receivable',
    is_disputed: true,
    order_id: 'order_id',
    principal_amount: {
      value: 'value',
    },
  },
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.CreateClaimRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ClaimsClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.claims.<a href="/src/api/resources/caseManagement/resources/claims/client/Client.ts">getEnforceableTitle</a>({ ...params }) -> Paywise.EnforceableTitleRead</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The enforceable-title singleton owned by a titled claim.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.claims.getEnforceableTitle({
  claim_id: 'claim_id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.GetEnforceableTitleRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ClaimsClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.claims.<a href="/src/api/resources/caseManagement/resources/claims/client/Client.ts">replaceEnforceableTitle</a>({ ...params }) -> Paywise.EnforceableTitleRead</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The enforceable-title singleton owned by a titled claim.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.claims.replaceEnforceableTitle({
  claim_id: 'claim_id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.EnforceableTitlePutRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ClaimsClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.claims.<a href="/src/api/resources/caseManagement/resources/claims/client/Client.ts">deleteEnforceableTitle</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The enforceable-title singleton owned by a titled claim.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.claims.deleteEnforceableTitle({
  claim_id: 'claim_id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.DeleteEnforceableTitleRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ClaimsClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.claims.<a href="/src/api/resources/caseManagement/resources/claims/client/Client.ts">updateEnforceableTitle</a>({ ...params }) -> Paywise.EnforceableTitleRead</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The enforceable-title singleton owned by a titled claim.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.claims.updateEnforceableTitle({
  claim_id: 'claim_id',
  legally_binding_since: '2026-02-15',
  served_on: '2026-02-12',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.PatchedEnforceableTitlePatchRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ClaimsClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.claims.<a href="/src/api/resources/caseManagement/resources/claims/client/Client.ts">listEnforceableTitleDocuments</a>({ ...params }) -> core.Page&lt;Paywise.DocumentRead, Paywise.PaginatedDocumentReadList&gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Documents owned by a titled claim's enforceable title.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse = await client.caseManagement.claims.listEnforceableTitleDocuments({
  claim_id: 'claim_id',
});
for await (const item of pageableResponse) {
  console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.caseManagement.claims.listEnforceableTitleDocuments({
  claim_id: 'claim_id',
});
while (page.hasNextPage()) {
  page = await page.getNextPage();
}

// You can also access the underlying response
const response = page.response;
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.ListEnforceableTitleDocumentsRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ClaimsClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.claims.<a href="/src/api/resources/caseManagement/resources/claims/client/Client.ts">createEnforceableTitleDocument</a>({ ...params }) -> Paywise.DocumentRead</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Documents owned by a titled claim's enforceable title.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.claims.createEnforceableTitleDocument({
  'Idempotency-Key': 'Idempotency-Key',
  claim_id: 'claim_id',
  type: 'enforceable_title',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.EnforceableTitleDocumentCreateRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ClaimsClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.claims.<a href="/src/api/resources/caseManagement/resources/claims/client/Client.ts">getEnforceableTitleDocument</a>({ ...params }) -> Paywise.DocumentRead</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Documents owned by a titled claim's enforceable title.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.claims.getEnforceableTitleDocument({
  claim_id: 'claim_id',
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.GetEnforceableTitleDocumentRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ClaimsClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.claims.<a href="/src/api/resources/caseManagement/resources/claims/client/Client.ts">deleteEnforceableTitleDocument</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Documents owned by a titled claim's enforceable title.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.claims.deleteEnforceableTitleDocument({
  claim_id: 'claim_id',
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.DeleteEnforceableTitleDocumentRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ClaimsClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.claims.<a href="/src/api/resources/caseManagement/resources/claims/client/Client.ts">downloadEnforceableTitleDocument</a>({ ...params }) -> core.BinaryResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Documents owned by a titled claim's enforceable title.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.claims.downloadEnforceableTitleDocument({
  claim_id: 'claim_id',
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.DownloadEnforceableTitleDocumentRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ClaimsClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.claims.<a href="/src/api/resources/caseManagement/resources/claims/client/Client.ts">listClaimPayments</a>({ ...params }) -> core.Page&lt;Paywise.PaymentRead, Paywise.PaginatedPaymentReadList&gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Client payments recorded on one claim across its whole lifecycle.

Draft and in-review orders take side-effect-free claim facts; once the
claim carries a mandate the create delegates to the shared claim payment
report. Deletion stays draft-only. Requires `case:payments:write` to report
or delete and `case:payments:read` to list, in every lifecycle state.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse = await client.caseManagement.claims.listClaimPayments({
  claim_id: 'claim_id',
});
for await (const item of pageableResponse) {
  console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.caseManagement.claims.listClaimPayments({
  claim_id: 'claim_id',
});
while (page.hasNextPage()) {
  page = await page.getNextPage();
}

// You can also access the underlying response
const response = page.response;
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.ListClaimPaymentsRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ClaimsClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.claims.<a href="/src/api/resources/caseManagement/resources/claims/client/Client.ts">createClaimPayment</a>({ ...params }) -> Paywise.PaymentRead</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Client payments recorded on one claim across its whole lifecycle.

Draft and in-review orders take side-effect-free claim facts; once the
claim carries a mandate the create delegates to the shared claim payment
report. Deletion stays draft-only. Requires `case:payments:write` to report
or delete and `case:payments:read` to list, in every lifecycle state.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.claims.createClaimPayment({
  'Idempotency-Key': 'Idempotency-Key',
  claim_id: 'claim_id',
  body: {
    amount: {
      currency: 'EUR',
      value: '50.00',
    },
    metadata: [
      {
        type: 'transaction:reference',
        value: 'BANK-TRANSACTION-99812',
      },
    ],
    value_date: '2026-07-17',
    your_reference: 'BANK-TRANSACTION-99812',
  },
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.CreateClaimPaymentRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ClaimsClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.claims.<a href="/src/api/resources/caseManagement/resources/claims/client/Client.ts">deleteClaimPayment</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Client payments recorded on one claim across its whole lifecycle.

Draft and in-review orders take side-effect-free claim facts; once the
claim carries a mandate the create delegates to the shared claim payment
report. Deletion stays draft-only. Requires `case:payments:write` to report
or delete and `case:payments:read` to list, in every lifecycle state.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.claims.deleteClaimPayment({
  claim_id: 'claim_id',
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.DeleteClaimPaymentRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ClaimsClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.claims.<a href="/src/api/resources/caseManagement/resources/claims/client/Client.ts">getClaim</a>({ ...params }) -> Paywise.Claim</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Claims addressed by their stable UUID and current relationships.

Read claims throughout their lifecycle using URLs that remain valid after
internal order moves. Standalone creation requires a draft `order_id`;
the relationship is read-only thereafter. Create, PATCH, and DELETE require
a draft order and otherwise return `409 claim_not_editable`. An expired
draft instead returns `409 order_expired`. Tenant-scoped by the
authenticated company.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.claims.getClaim({
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.GetClaimRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ClaimsClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.claims.<a href="/src/api/resources/caseManagement/resources/claims/client/Client.ts">deleteClaim</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Claims addressed by their stable UUID and current relationships.

Read claims throughout their lifecycle using URLs that remain valid after
internal order moves. Standalone creation requires a draft `order_id`;
the relationship is read-only thereafter. Create, PATCH, and DELETE require
a draft order and otherwise return `409 claim_not_editable`. An expired
draft instead returns `409 order_expired`. Tenant-scoped by the
authenticated company.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.claims.deleteClaim({
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.DeleteClaimRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ClaimsClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.claims.<a href="/src/api/resources/caseManagement/resources/claims/client/Client.ts">updateClaim</a>({ ...params }) -> Paywise.Claim</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Claims addressed by their stable UUID and current relationships.

Read claims throughout their lifecycle using URLs that remain valid after
internal order moves. Standalone creation requires a draft `order_id`;
the relationship is read-only thereafter. Create, PATCH, and DELETE require
a draft order and otherwise return `409 claim_not_editable`. An expired
draft instead returns `409 order_expired`. Tenant-scoped by the
authenticated company.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.claims.updateClaim({
  id: 'id',
  due_date: '2026-06-26',
  subject_matter: 'Website accessibility consulting in June 2026 (rev. 2)',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.PatchedClaimUpdateRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ClaimsClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## Documents

<details><summary><code>client.caseManagement.documents.<a href="/src/api/resources/caseManagement/resources/documents/client/Client.ts">listClaimDocuments</a>({ ...params }) -> core.Page&lt;Paywise.DocumentRead, Paywise.PaginatedDocumentReadList&gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Documents below one parent resource: upload, list, download, delete.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse = await client.caseManagement.documents.listClaimDocuments({
  claim_id: 'claim_id',
});
for await (const item of pageableResponse) {
  console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.caseManagement.documents.listClaimDocuments({
  claim_id: 'claim_id',
});
while (page.hasNextPage()) {
  page = await page.getNextPage();
}

// You can also access the underlying response
const response = page.response;
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.ListClaimDocumentsRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `DocumentsClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.documents.<a href="/src/api/resources/caseManagement/resources/documents/client/Client.ts">createClaimDocument</a>({ ...params }) -> Paywise.DocumentRead</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Documents below one parent resource: upload, list, download, delete.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.documents.createClaimDocument({
  'Idempotency-Key': 'Idempotency-Key',
  claim_id: 'claim_id',
  type: 'bank_statement',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.ClaimDocumentCreateRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `DocumentsClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.documents.<a href="/src/api/resources/caseManagement/resources/documents/client/Client.ts">getClaimDocument</a>({ ...params }) -> Paywise.DocumentRead</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Documents below one parent resource: upload, list, download, delete.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.documents.getClaimDocument({
  claim_id: 'claim_id',
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.GetClaimDocumentRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `DocumentsClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.documents.<a href="/src/api/resources/caseManagement/resources/documents/client/Client.ts">deleteClaimDocument</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Documents below one parent resource: upload, list, download, delete.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.documents.deleteClaimDocument({
  claim_id: 'claim_id',
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.DeleteClaimDocumentRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `DocumentsClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.documents.<a href="/src/api/resources/caseManagement/resources/documents/client/Client.ts">downloadClaimDocument</a>({ ...params }) -> core.BinaryResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Documents below one parent resource: upload, list, download, delete.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.documents.downloadClaimDocument({
  claim_id: 'claim_id',
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.DownloadClaimDocumentRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `DocumentsClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## Debtors

<details><summary><code>client.caseManagement.debtors.<a href="/src/api/resources/caseManagement/resources/debtors/client/Client.ts">listDebtors</a>({ ...params }) -> core.Page&lt;Paywise.DebtorList, Paywise.PaginatedDebtorListList&gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The reusable debtors of your company.

List, retrieve, create, and PATCH. A supplied owned collection
(addresses, bank accounts, communication channels, legal
representatives) replaces that collection completely; omitted
collections stay unchanged. A case's debtor is the case's own snapshot
(published as `MandateDebtor` without an id) and is not a reusable
debtor: it is neither listed nor readable here.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse = await client.caseManagement.debtors.listDebtors();
for await (const item of pageableResponse) {
  console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.caseManagement.debtors.listDebtors();
while (page.hasNextPage()) {
  page = await page.getNextPage();
}

// You can also access the underlying response
const response = page.response;
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.ListDebtorsRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `DebtorsClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.debtors.<a href="/src/api/resources/caseManagement/resources/debtors/client/Client.ts">createDebtor</a>({ ...params }) -> Paywise.DebtorDetail</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The reusable debtors of your company.

List, retrieve, create, and PATCH. A supplied owned collection
(addresses, bank accounts, communication channels, legal
representatives) replaces that collection completely; omitted
collections stay unchanged. A case's debtor is the case's own snapshot
(published as `MandateDebtor` without an id) and is not a reusable
debtor: it is neither listed nor readable here.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.debtors.createDebtor({
  'Idempotency-Key': 'Idempotency-Key',
  body: {
    acting_as: 'consumer',
    person: {
      first_name: 'first_name',
      last_name: 'last_name',
    },
  },
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.CreateDebtorRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `DebtorsClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.debtors.<a href="/src/api/resources/caseManagement/resources/debtors/client/Client.ts">getDebtor</a>({ ...params }) -> Paywise.DebtorDetail</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The reusable debtors of your company.

List, retrieve, create, and PATCH. A supplied owned collection
(addresses, bank accounts, communication channels, legal
representatives) replaces that collection completely; omitted
collections stay unchanged. A case's debtor is the case's own snapshot
(published as `MandateDebtor` without an id) and is not a reusable
debtor: it is neither listed nor readable here.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.debtors.getDebtor({
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.GetDebtorRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `DebtorsClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.debtors.<a href="/src/api/resources/caseManagement/resources/debtors/client/Client.ts">updateDebtor</a>({ ...params }) -> Paywise.DebtorDetail</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The reusable debtors of your company.

List, retrieve, create, and PATCH. A supplied owned collection
(addresses, bank accounts, communication channels, legal
representatives) replaces that collection completely; omitted
collections stay unchanged. A case's debtor is the case's own snapshot
(published as `MandateDebtor` without an id) and is not a reusable
debtor: it is neither listed nor readable here.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.debtors.updateDebtor({
  id: 'id',
  communication_channels: [
    {
      type: 'email',
      value: 'billing@example.test',
    },
    {
      type: 'mobile_phone',
      value: '+4915123456789',
    },
  ],
  your_reference: 'CUSTOMER-1001-UPDATED',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.PatchedDebtorWriteRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `DebtorsClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## Events

<details><summary><code>client.caseManagement.events.<a href="/src/api/resources/caseManagement/resources/events/client/Client.ts">listEvents</a>({ ...params }) -> core.Page&lt;Paywise.CaseWebhookEvent, Paywise.PaginatedEventFeed&gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return one page of the company's event feed, oldest first.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse = await client.caseManagement.events.listEvents();
for await (const item of pageableResponse) {
  console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.caseManagement.events.listEvents();
while (page.hasNextPage()) {
  page = await page.getNextPage();
}

// You can also access the underlying response
const response = page.response;
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.ListEventsRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EventsClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## Health

<details><summary><code>client.caseManagement.health.<a href="/src/api/resources/caseManagement/resources/health/client/Client.ts">check</a>() -> Paywise.CaseHealthResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return the unauthenticated Case Management API liveness response.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.health.check();
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `HealthClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## Info

<details><summary><code>client.caseManagement.info.<a href="/src/api/resources/caseManagement/resources/info/client/Client.ts">getCaseCredentialContext</a>() -> Paywise.CaseTokenInfoResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return non-PII metadata about the calling credential and selected company. Partner credentials must select the company through X-On-Behalf-Of-Company.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.info.getCaseCredentialContext();
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `InfoClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## Legal forms

<details><summary><code>client.caseManagement.legalForms.<a href="/src/api/resources/caseManagement/resources/legalForms/client/Client.ts">listLegalForms</a>({ ...params }) -> Paywise.LegalFormCatalog[]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return the authenticated, tenant-independent public catalog.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.legalForms.listLegalForms();
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.ListLegalFormsRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LegalFormsClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## Mandates

<details><summary><code>client.caseManagement.mandates.<a href="/src/api/resources/caseManagement/resources/mandates/client/Client.ts">listMandates</a>({ ...params }) -> core.Page&lt;Paywise.MandateList, Paywise.PaginatedMandateListList&gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Accepted cases (Aktenzeichen).

Main-case-centric: the list returns **main cases only**.
Sub-cases are reachable through the main case detail representation and
direct detail/subresource URLs, not a flat list expansion. Tenant-scoped by
the authenticated company.

Sub-resources of one mandate:

- payments — the reported, non-ignored payments
- documents — claim-document metadata and a proxy-stream download
- history — published client activity, related resources, and attachments.
  A main case includes its subcases; a subcase includes only itself.

The sub-resource operations resolve the mandate **including sub-cases** —
unlike the list, which hides sub-cases — so an individually-addressable
sub-case's own track stays reachable. These public mandate operations are
reads.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse = await client.caseManagement.mandates.listMandates();
for await (const item of pageableResponse) {
  console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.caseManagement.mandates.listMandates();
while (page.hasNextPage()) {
  page = await page.getNextPage();
}

// You can also access the underlying response
const response = page.response;
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.ListMandatesRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MandatesClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.mandates.<a href="/src/api/resources/caseManagement/resources/mandates/client/Client.ts">getMandate</a>({ ...params }) -> Paywise.MandateDetail</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Accepted cases (Aktenzeichen).

Main-case-centric: the list returns **main cases only**.
Sub-cases are reachable through the main case detail representation and
direct detail/subresource URLs, not a flat list expansion. Tenant-scoped by
the authenticated company.

Sub-resources of one mandate:

- payments — the reported, non-ignored payments
- documents — claim-document metadata and a proxy-stream download
- history — published client activity, related resources, and attachments.
  A main case includes its subcases; a subcase includes only itself.

The sub-resource operations resolve the mandate **including sub-cases** —
unlike the list, which hides sub-cases — so an individually-addressable
sub-case's own track stays reachable. These public mandate operations are
reads.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.mandates.getMandate({
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.GetMandateRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MandatesClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.mandates.<a href="/src/api/resources/caseManagement/resources/mandates/client/Client.ts">getMandateDocuments</a>({ ...params }) -> core.Page&lt;Paywise.MandateDocument, Paywise.MandateDocumentPage&gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Accepted cases (Aktenzeichen).

Main-case-centric: the list returns **main cases only**.
Sub-cases are reachable through the main case detail representation and
direct detail/subresource URLs, not a flat list expansion. Tenant-scoped by
the authenticated company.

Sub-resources of one mandate:

- payments — the reported, non-ignored payments
- documents — claim-document metadata and a proxy-stream download
- history — published client activity, related resources, and attachments.
  A main case includes its subcases; a subcase includes only itself.

The sub-resource operations resolve the mandate **including sub-cases** —
unlike the list, which hides sub-cases — so an individually-addressable
sub-case's own track stays reachable. These public mandate operations are
reads.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse = await client.caseManagement.mandates.getMandateDocuments({
  id: 'id',
});
for await (const item of pageableResponse) {
  console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.caseManagement.mandates.getMandateDocuments({
  id: 'id',
});
while (page.hasNextPage()) {
  page = await page.getNextPage();
}

// You can also access the underlying response
const response = page.response;
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.GetMandateDocumentsRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MandatesClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.mandates.<a href="/src/api/resources/caseManagement/resources/mandates/client/Client.ts">downloadMandateDocument</a>({ ...params }) -> core.BinaryResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Accepted cases (Aktenzeichen).

Main-case-centric: the list returns **main cases only**.
Sub-cases are reachable through the main case detail representation and
direct detail/subresource URLs, not a flat list expansion. Tenant-scoped by
the authenticated company.

Sub-resources of one mandate:

- payments — the reported, non-ignored payments
- documents — claim-document metadata and a proxy-stream download
- history — published client activity, related resources, and attachments.
  A main case includes its subcases; a subcase includes only itself.

The sub-resource operations resolve the mandate **including sub-cases** —
unlike the list, which hides sub-cases — so an individually-addressable
sub-case's own track stays reachable. These public mandate operations are
reads.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.mandates.downloadMandateDocument({
  id: 'id',
  doc_id: 'doc_id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.DownloadMandateDocumentRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MandatesClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.mandates.<a href="/src/api/resources/caseManagement/resources/mandates/client/Client.ts">getMandateHistory</a>({ ...params }) -> core.Page&lt;Paywise.MandateHistory, Paywise.MandateHistoryPage&gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Accepted cases (Aktenzeichen).

Main-case-centric: the list returns **main cases only**.
Sub-cases are reachable through the main case detail representation and
direct detail/subresource URLs, not a flat list expansion. Tenant-scoped by
the authenticated company.

Sub-resources of one mandate:

- payments — the reported, non-ignored payments
- documents — claim-document metadata and a proxy-stream download
- history — published client activity, related resources, and attachments.
  A main case includes its subcases; a subcase includes only itself.

The sub-resource operations resolve the mandate **including sub-cases** —
unlike the list, which hides sub-cases — so an individually-addressable
sub-case's own track stays reachable. These public mandate operations are
reads.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse = await client.caseManagement.mandates.getMandateHistory({
  id: 'id',
});
for await (const item of pageableResponse) {
  console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.caseManagement.mandates.getMandateHistory({
  id: 'id',
});
while (page.hasNextPage()) {
  page = await page.getNextPage();
}

// You can also access the underlying response
const response = page.response;
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.GetMandateHistoryRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MandatesClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.mandates.<a href="/src/api/resources/caseManagement/resources/mandates/client/Client.ts">downloadMandateHistoryAttachment</a>({ ...params }) -> core.BinaryResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Download a file explicitly published with a history entry. The entry must belong to the selected mandate's history: main case plus its subcases for a main-case URL, or only the selected subcase.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.mandates.downloadMandateHistoryAttachment({
  id: 'id',
  entry_id: 'entry_id',
  file_id: 'file_id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.DownloadMandateHistoryAttachmentRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MandatesClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.mandates.<a href="/src/api/resources/caseManagement/resources/mandates/client/Client.ts">listMandateMessages</a>({ ...params }) -> core.Page&lt;Paywise.MessageRead, Paywise.PaginatedMessageReadList&gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Messages exchanged with paywise about one order or one case.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse = await client.caseManagement.mandates.listMandateMessages({
  mandate_id: 'mandate_id',
});
for await (const item of pageableResponse) {
  console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.caseManagement.mandates.listMandateMessages({
  mandate_id: 'mandate_id',
});
while (page.hasNextPage()) {
  page = await page.getNextPage();
}

// You can also access the underlying response
const response = page.response;
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.ListMandateMessagesRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MandatesClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.mandates.<a href="/src/api/resources/caseManagement/resources/mandates/client/Client.ts">createMandateMessage</a>({ ...params }) -> Paywise.MessageRead</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Messages exchanged with paywise about one order or one case.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.mandates.createMandateMessage({
  'Idempotency-Key': 'Idempotency-Key',
  mandate_id: 'mandate_id',
  body: {
    body: 'The customer provided an updated invoice address.',
    documents: [
      {
        base64: 'base64',
        type: 'bank_statement',
      },
    ],
    title: 'Updated invoice address',
  },
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.CreateMandateMessageRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MandatesClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.mandates.<a href="/src/api/resources/caseManagement/resources/mandates/client/Client.ts">getMandateMessage</a>({ ...params }) -> Paywise.MessageRead</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Messages exchanged with paywise about one order or one case.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.mandates.getMandateMessage({
  mandate_id: 'mandate_id',
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.GetMandateMessageRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MandatesClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.mandates.<a href="/src/api/resources/caseManagement/resources/mandates/client/Client.ts">updateMandateMessage</a>({ ...params }) -> Paywise.MessageRead</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Messages exchanged with paywise about one order or one case.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.mandates.updateMandateMessage({
  mandate_id: 'mandate_id',
  id: 'id',
  body: {
    body: 'Correction: the new invoice address applies from 1 August 2026.',
    title: 'Updated invoice address (corrected)',
  },
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.UpdateMandateMessageRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MandatesClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.mandates.<a href="/src/api/resources/caseManagement/resources/mandates/client/Client.ts">listMandateMessageDocuments</a>({ ...params }) -> core.Page&lt;Paywise.DocumentRead, Paywise.PaginatedDocumentReadList&gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Documents below one parent resource: upload, list, download, delete.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse = await client.caseManagement.mandates.listMandateMessageDocuments({
  mandate_id: 'mandate_id',
  message_id: 'message_id',
});
for await (const item of pageableResponse) {
  console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.caseManagement.mandates.listMandateMessageDocuments({
  mandate_id: 'mandate_id',
  message_id: 'message_id',
});
while (page.hasNextPage()) {
  page = await page.getNextPage();
}

// You can also access the underlying response
const response = page.response;
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.ListMandateMessageDocumentsRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MandatesClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.mandates.<a href="/src/api/resources/caseManagement/resources/mandates/client/Client.ts">createMandateMessageDocument</a>({ ...params }) -> Paywise.DocumentRead</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Documents below one parent resource: upload, list, download, delete.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.mandates.createMandateMessageDocument({
  'Idempotency-Key': 'Idempotency-Key',
  mandate_id: 'mandate_id',
  message_id: 'message_id',
  type: 'bank_statement',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.CreateMandateMessageDocumentRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MandatesClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.mandates.<a href="/src/api/resources/caseManagement/resources/mandates/client/Client.ts">getMandateMessageDocument</a>({ ...params }) -> Paywise.DocumentRead</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Documents below one parent resource: upload, list, download, delete.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.mandates.getMandateMessageDocument({
  mandate_id: 'mandate_id',
  message_id: 'message_id',
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.GetMandateMessageDocumentRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MandatesClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.mandates.<a href="/src/api/resources/caseManagement/resources/mandates/client/Client.ts">deleteMandateMessageDocument</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Documents below one parent resource: upload, list, download, delete.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.mandates.deleteMandateMessageDocument({
  mandate_id: 'mandate_id',
  message_id: 'message_id',
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.DeleteMandateMessageDocumentRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MandatesClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.mandates.<a href="/src/api/resources/caseManagement/resources/mandates/client/Client.ts">downloadMandateMessageDocument</a>({ ...params }) -> core.BinaryResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Documents below one parent resource: upload, list, download, delete.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.mandates.downloadMandateMessageDocument({
  mandate_id: 'mandate_id',
  message_id: 'message_id',
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.DownloadMandateMessageDocumentRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MandatesClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.mandates.<a href="/src/api/resources/caseManagement/resources/mandates/client/Client.ts">listMandatePayments</a>({ ...params }) -> core.Page&lt;Paywise.PaymentRead, Paywise.PaginatedPaymentReadList&gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Immutable client payment reports under a main mandate or subcase.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse = await client.caseManagement.mandates.listMandatePayments({
  mandate_id: 'mandate_id',
});
for await (const item of pageableResponse) {
  console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.caseManagement.mandates.listMandatePayments({
  mandate_id: 'mandate_id',
});
while (page.hasNextPage()) {
  page = await page.getNextPage();
}

// You can also access the underlying response
const response = page.response;
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.ListMandatePaymentsRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MandatesClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.mandates.<a href="/src/api/resources/caseManagement/resources/mandates/client/Client.ts">createMandatePayment</a>({ ...params }) -> Paywise.PaymentRead</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Immutable client payment reports under a main mandate or subcase.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.mandates.createMandatePayment({
  'Idempotency-Key': 'Idempotency-Key',
  mandate_id: 'mandate_id',
  body: {
    amount: {
      currency: 'EUR',
      value: '50.00',
    },
    metadata: [
      {
        type: 'transaction:reference',
        value: 'BANK-TRANSACTION-99812',
      },
    ],
    value_date: '2026-07-17',
    your_reference: 'BANK-TRANSACTION-99812',
  },
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.CreateMandatePaymentRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MandatesClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.mandates.<a href="/src/api/resources/caseManagement/resources/mandates/client/Client.ts">listMandateRequestsToClient</a>({ ...params }) -> core.Page&lt;Paywise.RequestToClientRead, Paywise.PaginatedRequestToClientReadList&gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Published questions paywise asks the client about one case.

list/retrieve, plus `answer` to respond exactly once per request.
Tenant-scoped by the authenticated company; only published requests are
visible.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse = await client.caseManagement.mandates.listMandateRequestsToClient({
  mandate_id: 'mandate_id',
});
for await (const item of pageableResponse) {
  console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.caseManagement.mandates.listMandateRequestsToClient({
  mandate_id: 'mandate_id',
});
while (page.hasNextPage()) {
  page = await page.getNextPage();
}

// You can also access the underlying response
const response = page.response;
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.ListMandateRequestsToClientRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MandatesClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.mandates.<a href="/src/api/resources/caseManagement/resources/mandates/client/Client.ts">getMandateRequestToClient</a>({ ...params }) -> Paywise.RequestToClientRead</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Published questions paywise asks the client about one case.

list/retrieve, plus `answer` to respond exactly once per request.
Tenant-scoped by the authenticated company; only published requests are
visible.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.mandates.getMandateRequestToClient({
  mandate_id: 'mandate_id',
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.GetMandateRequestToClientRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MandatesClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.mandates.<a href="/src/api/resources/caseManagement/resources/mandates/client/Client.ts">answerMandateRequestToClient</a>({ ...params }) -> Paywise.RequestToClientRead</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Published questions paywise asks the client about one case.

list/retrieve, plus `answer` to respond exactly once per request.
Tenant-scoped by the authenticated company; only published requests are
visible.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.mandates.answerMandateRequestToClient({
  'Idempotency-Key': 'Idempotency-Key',
  mandate_id: 'mandate_id',
  id: 'id',
  body: {
    additional_comment: 'Please continue processing.',
    documents: [
      {
        base64: 'base64',
        type: 'bank_statement',
      },
    ],
    text: 'The outstanding amount is correct.',
  },
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.AnswerMandateRequestToClientRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MandatesClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.mandates.<a href="/src/api/resources/caseManagement/resources/mandates/client/Client.ts">downloadMandateRequestToClientAttachment</a>({ ...params }) -> core.BinaryResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Proxy-stream one of the question's case-worker attachments.

Attachments are resolved through the tenant-scoped request itself,
so a caller can only reach attachments on a request its company owns.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.mandates.downloadMandateRequestToClientAttachment({
  mandate_id: 'mandate_id',
  id: 'id',
  attachment_id: 'attachment_id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.DownloadMandateRequestToClientAttachmentRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MandatesClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.mandates.<a href="/src/api/resources/caseManagement/resources/mandates/client/Client.ts">listMandateRequestToClientAnswerDocuments</a>({ ...params }) -> core.Page&lt;Paywise.DocumentRead, Paywise.PaginatedDocumentReadList&gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Documents added to one v2 answer before its review task starts.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse =
  await client.caseManagement.mandates.listMandateRequestToClientAnswerDocuments({
    mandate_id: 'mandate_id',
    request_id: 'request_id',
  });
for await (const item of pageableResponse) {
  console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.caseManagement.mandates.listMandateRequestToClientAnswerDocuments({
  mandate_id: 'mandate_id',
  request_id: 'request_id',
});
while (page.hasNextPage()) {
  page = await page.getNextPage();
}

// You can also access the underlying response
const response = page.response;
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.ListMandateRequestToClientAnswerDocumentsRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MandatesClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.mandates.<a href="/src/api/resources/caseManagement/resources/mandates/client/Client.ts">createMandateRequestToClientAnswerDocument</a>({ ...params }) -> Paywise.DocumentRead</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Documents added to one v2 answer before its review task starts.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.mandates.createMandateRequestToClientAnswerDocument({
  'Idempotency-Key': 'Idempotency-Key',
  mandate_id: 'mandate_id',
  request_id: 'request_id',
  type: 'bank_statement',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.CreateMandateRequestToClientAnswerDocumentRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MandatesClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.mandates.<a href="/src/api/resources/caseManagement/resources/mandates/client/Client.ts">getMandateRequestToClientAnswerDocument</a>({ ...params }) -> Paywise.DocumentRead</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Documents added to one v2 answer before its review task starts.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.mandates.getMandateRequestToClientAnswerDocument({
  mandate_id: 'mandate_id',
  request_id: 'request_id',
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.GetMandateRequestToClientAnswerDocumentRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MandatesClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.mandates.<a href="/src/api/resources/caseManagement/resources/mandates/client/Client.ts">deleteMandateRequestToClientAnswerDocument</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Documents added to one v2 answer before its review task starts.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.mandates.deleteMandateRequestToClientAnswerDocument({
  mandate_id: 'mandate_id',
  request_id: 'request_id',
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.DeleteMandateRequestToClientAnswerDocumentRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MandatesClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.mandates.<a href="/src/api/resources/caseManagement/resources/mandates/client/Client.ts">downloadMandateRequestToClientAnswerDocument</a>({ ...params }) -> core.BinaryResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Documents added to one v2 answer before its review task starts.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.mandates.downloadMandateRequestToClientAnswerDocument({
  mandate_id: 'mandate_id',
  request_id: 'request_id',
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.DownloadMandateRequestToClientAnswerDocumentRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MandatesClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## Orders

<details><summary><code>client.caseManagement.orders.<a href="/src/api/resources/caseManagement/resources/orders/client/Client.ts">listOrders</a>({ ...params }) -> core.Page&lt;Paywise.Order, Paywise.PaginatedOrderList&gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The collection orders of your company.

Create a draft with a referenced debtor and embedded claims,
edit it while it is a draft, finalize it for review, and follow it to
acceptance. Tenant-scoped by the authenticated company.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse = await client.caseManagement.orders.listOrders();
for await (const item of pageableResponse) {
  console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.caseManagement.orders.listOrders();
while (page.hasNextPage()) {
  page = await page.getNextPage();
}

// You can also access the underlying response
const response = page.response;
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.ListOrdersRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.orders.<a href="/src/api/resources/caseManagement/resources/orders/client/Client.ts">createOrder</a>({ ...params }) -> Paywise.Order</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The collection orders of your company.

Create a draft with a referenced debtor and embedded claims,
edit it while it is a draft, finalize it for review, and follow it to
acceptance. Tenant-scoped by the authenticated company.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.orders.createOrder({
  'Idempotency-Key': 'Idempotency-Key',
  additional_debtor_ids: ['additional_debtor_ids'],
  claims: [
    {
      type: 'receivable',
      is_disputed: true,
      principal_amount: {
        value: 'value',
      },
    },
  ],
  creditor_obligation_fulfilled: true,
  debtor_id: '40000000-0000-4000-8000-000000000001',
  starting_approach: 'extrajudicial',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.OrderCreateRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.orders.<a href="/src/api/resources/caseManagement/resources/orders/client/Client.ts">getOrder</a>({ ...params }) -> Paywise.Order</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The collection orders of your company.

Create a draft with a referenced debtor and embedded claims,
edit it while it is a draft, finalize it for review, and follow it to
acceptance. Tenant-scoped by the authenticated company.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.orders.getOrder({
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.GetOrderRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.orders.<a href="/src/api/resources/caseManagement/resources/orders/client/Client.ts">deleteDraftOrder</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The collection orders of your company.

Create a draft with a referenced debtor and embedded claims,
edit it while it is a draft, finalize it for review, and follow it to
acceptance. Tenant-scoped by the authenticated company.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.orders.deleteDraftOrder({
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.DeleteDraftOrderRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.orders.<a href="/src/api/resources/caseManagement/resources/orders/client/Client.ts">updateOrder</a>({ ...params }) -> Paywise.Order</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update the order's mutable fields while it is a draft.

A supplied `additional_debtor_ids` array replaces its membership; omit it
to preserve the links or send `[]` to unlink all additional debtors
without deleting their records. Read full debtor details through
`GET /v2/debtors/{id}/`.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.orders.updateOrder({
  id: 'id',
  confirmation_email: 'billing@example.test',
  starting_approach: 'extrajudicial',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.PatchedOrderDecisionPatchRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.orders.<a href="/src/api/resources/caseManagement/resources/orders/client/Client.ts">finalizeOrder</a>({ ...params }) -> Paywise.Order</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Finalize the order: validates the complete aggregate, makes it
immutable, and submits it for review. Declares no request body.
Acceptance happens later during review and is announced via
`order.accepted`.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.orders.finalizeOrder({
  'Idempotency-Key': 'Idempotency-Key',
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.FinalizeOrderRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.orders.<a href="/src/api/resources/caseManagement/resources/orders/client/Client.ts">withdrawOrder</a>({ ...params }) -> Paywise.Order</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Withdraw one submitted order before staff acceptance starts.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.orders.withdrawOrder({
  'Idempotency-Key': 'Idempotency-Key',
  id: 'id',
  reason: 'The customer paid before review began.',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.OrderWithdrawRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.orders.<a href="/src/api/resources/caseManagement/resources/orders/client/Client.ts">listOrderMessages</a>({ ...params }) -> core.Page&lt;Paywise.MessageRead, Paywise.PaginatedMessageReadList&gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Messages exchanged with paywise about one order or one case.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse = await client.caseManagement.orders.listOrderMessages({
  order_id: 'order_id',
});
for await (const item of pageableResponse) {
  console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.caseManagement.orders.listOrderMessages({
  order_id: 'order_id',
});
while (page.hasNextPage()) {
  page = await page.getNextPage();
}

// You can also access the underlying response
const response = page.response;
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.ListOrderMessagesRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.orders.<a href="/src/api/resources/caseManagement/resources/orders/client/Client.ts">createOrderMessage</a>({ ...params }) -> Paywise.MessageRead</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Messages exchanged with paywise about one order or one case.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.orders.createOrderMessage({
  'Idempotency-Key': 'Idempotency-Key',
  order_id: 'order_id',
  body: {
    body: 'The customer provided an updated invoice address.',
    documents: [
      {
        base64: 'base64',
        type: 'bank_statement',
      },
    ],
    title: 'Updated invoice address',
  },
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.CreateOrderMessageRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.orders.<a href="/src/api/resources/caseManagement/resources/orders/client/Client.ts">getOrderMessage</a>({ ...params }) -> Paywise.MessageRead</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Messages exchanged with paywise about one order or one case.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.orders.getOrderMessage({
  order_id: 'order_id',
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.GetOrderMessageRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.orders.<a href="/src/api/resources/caseManagement/resources/orders/client/Client.ts">updateOrderMessage</a>({ ...params }) -> Paywise.MessageRead</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Messages exchanged with paywise about one order or one case.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.orders.updateOrderMessage({
  order_id: 'order_id',
  id: 'id',
  body: {
    body: 'Correction: the new invoice address applies from 1 August 2026.',
    title: 'Updated invoice address (corrected)',
  },
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.UpdateOrderMessageRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.orders.<a href="/src/api/resources/caseManagement/resources/orders/client/Client.ts">listOrderMessageDocuments</a>({ ...params }) -> core.Page&lt;Paywise.DocumentRead, Paywise.PaginatedDocumentReadList&gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Documents below one parent resource: upload, list, download, delete.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse = await client.caseManagement.orders.listOrderMessageDocuments({
  order_id: 'order_id',
  message_id: 'message_id',
});
for await (const item of pageableResponse) {
  console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.caseManagement.orders.listOrderMessageDocuments({
  order_id: 'order_id',
  message_id: 'message_id',
});
while (page.hasNextPage()) {
  page = await page.getNextPage();
}

// You can also access the underlying response
const response = page.response;
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.ListOrderMessageDocumentsRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.orders.<a href="/src/api/resources/caseManagement/resources/orders/client/Client.ts">createOrderMessageDocument</a>({ ...params }) -> Paywise.DocumentRead</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Documents below one parent resource: upload, list, download, delete.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.orders.createOrderMessageDocument({
  'Idempotency-Key': 'Idempotency-Key',
  order_id: 'order_id',
  message_id: 'message_id',
  type: 'bank_statement',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.CreateOrderMessageDocumentRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.orders.<a href="/src/api/resources/caseManagement/resources/orders/client/Client.ts">getOrderMessageDocument</a>({ ...params }) -> Paywise.DocumentRead</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Documents below one parent resource: upload, list, download, delete.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.orders.getOrderMessageDocument({
  order_id: 'order_id',
  message_id: 'message_id',
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.GetOrderMessageDocumentRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.orders.<a href="/src/api/resources/caseManagement/resources/orders/client/Client.ts">deleteOrderMessageDocument</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Documents below one parent resource: upload, list, download, delete.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.orders.deleteOrderMessageDocument({
  order_id: 'order_id',
  message_id: 'message_id',
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.DeleteOrderMessageDocumentRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.orders.<a href="/src/api/resources/caseManagement/resources/orders/client/Client.ts">downloadOrderMessageDocument</a>({ ...params }) -> core.BinaryResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Documents below one parent resource: upload, list, download, delete.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.orders.downloadOrderMessageDocument({
  order_id: 'order_id',
  message_id: 'message_id',
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.DownloadOrderMessageDocumentRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.orders.<a href="/src/api/resources/caseManagement/resources/orders/client/Client.ts">getRentalAgreement</a>({ ...params }) -> Paywise.RentalAgreementRead</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Tenant-scoped resource collection of the authenticated company.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.orders.getRentalAgreement({
  order_id: 'order_id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.GetRentalAgreementRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.orders.<a href="/src/api/resources/caseManagement/resources/orders/client/Client.ts">updateRentalAgreement</a>({ ...params }) -> Paywise.RentalAgreementRead</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Tenant-scoped resource collection of the authenticated company.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.orders.updateRentalAgreement({
  order_id: 'order_id',
  due_rule: {
    day: 5,
    kind: 'business_day',
  },
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.PatchedRentalAgreementWriteRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.orders.<a href="/src/api/resources/caseManagement/resources/orders/client/Client.ts">listRentalAgreementDocuments</a>({ ...params }) -> core.Page&lt;Paywise.DocumentRead, Paywise.PaginatedDocumentReadList&gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Documents owned by a rental order's agreement singleton.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse = await client.caseManagement.orders.listRentalAgreementDocuments({
  order_id: 'order_id',
});
for await (const item of pageableResponse) {
  console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.caseManagement.orders.listRentalAgreementDocuments({
  order_id: 'order_id',
});
while (page.hasNextPage()) {
  page = await page.getNextPage();
}

// You can also access the underlying response
const response = page.response;
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.ListRentalAgreementDocumentsRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.orders.<a href="/src/api/resources/caseManagement/resources/orders/client/Client.ts">createRentalAgreementDocument</a>({ ...params }) -> Paywise.DocumentRead</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Documents owned by a rental order's agreement singleton.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.orders.createRentalAgreementDocument({
  'Idempotency-Key': 'Idempotency-Key',
  order_id: 'order_id',
  type: 'rental_agreement',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.RentalAgreementDocumentCreateRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.orders.<a href="/src/api/resources/caseManagement/resources/orders/client/Client.ts">getRentalAgreementDocument</a>({ ...params }) -> Paywise.DocumentRead</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Documents owned by a rental order's agreement singleton.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.orders.getRentalAgreementDocument({
  order_id: 'order_id',
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.GetRentalAgreementDocumentRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.orders.<a href="/src/api/resources/caseManagement/resources/orders/client/Client.ts">deleteRentalAgreementDocument</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Documents owned by a rental order's agreement singleton.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.orders.deleteRentalAgreementDocument({
  order_id: 'order_id',
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.DeleteRentalAgreementDocumentRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.orders.<a href="/src/api/resources/caseManagement/resources/orders/client/Client.ts">downloadRentalAgreementDocument</a>({ ...params }) -> core.BinaryResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Documents owned by a rental order's agreement singleton.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.orders.downloadRentalAgreementDocument({
  order_id: 'order_id',
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.DownloadRentalAgreementDocumentRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.orders.<a href="/src/api/resources/caseManagement/resources/orders/client/Client.ts">listOrderRequestsToClient</a>({ ...params }) -> core.Page&lt;Paywise.OrderRequestToClientRead, Paywise.PaginatedOrderRequestToClientReadList&gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Published questions about one order, including orders awaiting review.

Answer once using the advertised answer type. Closed orders reject answers
with 409. Review resumes after all published requests are answered.
Documents become downloadable when ready. Only the authenticated company's published requests
are visible.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse = await client.caseManagement.orders.listOrderRequestsToClient({
  order_id: 'order_id',
});
for await (const item of pageableResponse) {
  console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.caseManagement.orders.listOrderRequestsToClient({
  order_id: 'order_id',
});
while (page.hasNextPage()) {
  page = await page.getNextPage();
}

// You can also access the underlying response
const response = page.response;
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.ListOrderRequestsToClientRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.orders.<a href="/src/api/resources/caseManagement/resources/orders/client/Client.ts">getOrderRequestToClient</a>({ ...params }) -> Paywise.OrderRequestToClientRead</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Published questions about one order, including orders awaiting review.

Answer once using the advertised answer type. Closed orders reject answers
with 409. Review resumes after all published requests are answered.
Documents become downloadable when ready. Only the authenticated company's published requests
are visible.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.orders.getOrderRequestToClient({
  order_id: 'order_id',
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.GetOrderRequestToClientRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.orders.<a href="/src/api/resources/caseManagement/resources/orders/client/Client.ts">answerOrderRequestToClient</a>({ ...params }) -> Paywise.OrderRequestToClientRead</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Published questions about one order, including orders awaiting review.

Answer once using the advertised answer type. Closed orders reject answers
with 409. Review resumes after all published requests are answered.
Documents become downloadable when ready. Only the authenticated company's published requests
are visible.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.orders.answerOrderRequestToClient({
  'Idempotency-Key': 'Idempotency-Key',
  order_id: 'order_id',
  id: 'id',
  body: {
    additional_comment: 'The invoice is correct.',
    documents: [
      {
        base64: 'base64',
        type: 'bank_statement',
      },
    ],
    text: 'yes',
  },
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.AnswerOrderRequestToClientRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.orders.<a href="/src/api/resources/caseManagement/resources/orders/client/Client.ts">downloadOrderRequestToClientAttachment</a>({ ...params }) -> core.BinaryResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Proxy-stream one of the question's case-worker attachments.

Attachments are resolved through the tenant-scoped request itself,
so a caller can only reach attachments on a request its company owns.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.orders.downloadOrderRequestToClientAttachment({
  order_id: 'order_id',
  id: 'id',
  attachment_id: 'attachment_id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.DownloadOrderRequestToClientAttachmentRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.orders.<a href="/src/api/resources/caseManagement/resources/orders/client/Client.ts">listOrderRequestToClientAnswerDocuments</a>({ ...params }) -> core.Page&lt;Paywise.DocumentRead, Paywise.PaginatedDocumentReadList&gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Documents on an order request answer, editable until staff review starts.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse = await client.caseManagement.orders.listOrderRequestToClientAnswerDocuments(
  {
    order_id: 'order_id',
    request_id: 'request_id',
  },
);
for await (const item of pageableResponse) {
  console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.caseManagement.orders.listOrderRequestToClientAnswerDocuments({
  order_id: 'order_id',
  request_id: 'request_id',
});
while (page.hasNextPage()) {
  page = await page.getNextPage();
}

// You can also access the underlying response
const response = page.response;
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.ListOrderRequestToClientAnswerDocumentsRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.orders.<a href="/src/api/resources/caseManagement/resources/orders/client/Client.ts">createOrderRequestToClientAnswerDocument</a>({ ...params }) -> Paywise.DocumentRead</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Documents on an order request answer, editable until staff review starts.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.orders.createOrderRequestToClientAnswerDocument({
  'Idempotency-Key': 'Idempotency-Key',
  order_id: 'order_id',
  request_id: 'request_id',
  type: 'bank_statement',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.CreateOrderRequestToClientAnswerDocumentRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.orders.<a href="/src/api/resources/caseManagement/resources/orders/client/Client.ts">getOrderRequestToClientAnswerDocument</a>({ ...params }) -> Paywise.DocumentRead</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Documents on an order request answer, editable until staff review starts.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.orders.getOrderRequestToClientAnswerDocument({
  order_id: 'order_id',
  request_id: 'request_id',
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.GetOrderRequestToClientAnswerDocumentRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.orders.<a href="/src/api/resources/caseManagement/resources/orders/client/Client.ts">deleteOrderRequestToClientAnswerDocument</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Documents on an order request answer, editable until staff review starts.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.orders.deleteOrderRequestToClientAnswerDocument({
  order_id: 'order_id',
  request_id: 'request_id',
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.DeleteOrderRequestToClientAnswerDocumentRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.orders.<a href="/src/api/resources/caseManagement/resources/orders/client/Client.ts">downloadOrderRequestToClientAnswerDocument</a>({ ...params }) -> core.BinaryResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Documents on an order request answer, editable until staff review starts.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.orders.downloadOrderRequestToClientAnswerDocument({
  order_id: 'order_id',
  request_id: 'request_id',
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.DownloadOrderRequestToClientAnswerDocumentRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdersClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## Payments

<details><summary><code>client.caseManagement.payments.<a href="/src/api/resources/caseManagement/resources/payments/client/Client.ts">listPayments</a>({ ...params }) -> core.Page&lt;Paywise.PaymentRead, Paywise.PaginatedPaymentReadList&gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Read-only top-level payment collection.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse = await client.caseManagement.payments.listPayments();
for await (const item of pageableResponse) {
  console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.caseManagement.payments.listPayments();
while (page.hasNextPage()) {
  page = await page.getNextPage();
}

// You can also access the underlying response
const response = page.response;
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.ListPaymentsRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PaymentsClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.payments.<a href="/src/api/resources/caseManagement/resources/payments/client/Client.ts">getPayment</a>({ ...params }) -> Paywise.PaymentRead</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Read-only top-level payment collection.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.payments.getPayment({
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.GetPaymentRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PaymentsClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## Single mandate statements

<details><summary><code>client.caseManagement.singleMandateStatements.<a href="/src/api/resources/caseManagement/resources/singleMandateStatements/client/Client.ts">listSingleMandateStatements</a>({ ...params }) -> core.Page&lt;Paywise.SingleMandateStatementList, Paywise.PaginatedSingleMandateStatementListList&gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Published per-case settlements (Aktenabrechnungen) and their PDF.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse =
  await client.caseManagement.singleMandateStatements.listSingleMandateStatements();
for await (const item of pageableResponse) {
  console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.caseManagement.singleMandateStatements.listSingleMandateStatements();
while (page.hasNextPage()) {
  page = await page.getNextPage();
}

// You can also access the underlying response
const response = page.response;
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.ListSingleMandateStatementsRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SingleMandateStatementsClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.singleMandateStatements.<a href="/src/api/resources/caseManagement/resources/singleMandateStatements/client/Client.ts">getSingleMandateStatement</a>({ ...params }) -> Paywise.SingleMandateStatementRead</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Published per-case settlements (Aktenabrechnungen) and their PDF.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.singleMandateStatements.getSingleMandateStatement({
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.GetSingleMandateStatementRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SingleMandateStatementsClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.singleMandateStatements.<a href="/src/api/resources/caseManagement/resources/singleMandateStatements/client/Client.ts">downloadSingleMandateStatementPdf</a>({ ...params }) -> core.BinaryResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Proxy the stored PDF without disclosing its storage location.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.singleMandateStatements.downloadSingleMandateStatementPdf({
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.DownloadSingleMandateStatementPdfRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `SingleMandateStatementsClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## Statements

<details><summary><code>client.caseManagement.statements.<a href="/src/api/resources/caseManagement/resources/statements/client/Client.ts">listStatements</a>({ ...params }) -> core.Page&lt;Paywise.StatementList, Paywise.PaginatedStatementListList&gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Published payout statements and their customer-visible breakdown.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse = await client.caseManagement.statements.listStatements();
for await (const item of pageableResponse) {
  console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.caseManagement.statements.listStatements();
while (page.hasNextPage()) {
  page = await page.getNextPage();
}

// You can also access the underlying response
const response = page.response;
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.ListStatementsRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `StatementsClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.statements.<a href="/src/api/resources/caseManagement/resources/statements/client/Client.ts">getStatement</a>({ ...params }) -> Paywise.StatementRead</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Published payout statements and their customer-visible breakdown.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.statements.getStatement({
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.GetStatementRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `StatementsClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.statements.<a href="/src/api/resources/caseManagement/resources/statements/client/Client.ts">downloadStatement</a>({ ...params }) -> core.BinaryResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Proxy one stored statement file without disclosing its storage location.

The type parameter selects the PDF (default) or one of the three
Excel exports; a type whose file has not been transferred is 404.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.statements.downloadStatement({
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.DownloadStatementRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `StatementsClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.statements.<a href="/src/api/resources/caseManagement/resources/statements/client/Client.ts">listStatementCases</a>({ ...params }) -> core.Page&lt;Paywise.StatementMandateRow, Paywise.StatementMandateRowPage&gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Page through the accepted cases included in one statement.

Same rows as the mandates array of the statement detail, with
limit/offset pagination and filters on the case and claim references.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse = await client.caseManagement.statements.listStatementCases({
  id: 'id',
});
for await (const item of pageableResponse) {
  console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.caseManagement.statements.listStatementCases({
  id: 'id',
});
while (page.hasNextPage()) {
  page = await page.getNextPage();
}

// You can also access the underlying response
const response = page.response;
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.ListStatementCasesRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `StatementsClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## Usage

<details><summary><code>client.caseManagement.usage.<a href="/src/api/resources/caseManagement/resources/usage/client/Client.ts">getRateLimitHeadroom</a>() -> Paywise.UsageResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return an authoritative point-in-time snapshot of every rate-limit bucket applicable to the authenticated Case credential. The call itself counts against each applicable principal bucket: the token, the Partner for delegated traffic, and the active company.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.usage.getRateLimitHeadroom();
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `UsageClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## Webhook deliveries

<details><summary><code>client.caseManagement.webhookDeliveries.<a href="/src/api/resources/caseManagement/resources/webhookDeliveries/client/Client.ts">listWebhookDeliveries</a>({ ...params }) -> core.Page&lt;Paywise.WebhookDelivery, Paywise.PaginatedWebhookDeliveryList&gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Read-only webhook delivery log, plus manual redelivery.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse = await client.caseManagement.webhookDeliveries.listWebhookDeliveries();
for await (const item of pageableResponse) {
  console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.caseManagement.webhookDeliveries.listWebhookDeliveries();
while (page.hasNextPage()) {
  page = await page.getNextPage();
}

// You can also access the underlying response
const response = page.response;
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.ListWebhookDeliveriesRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WebhookDeliveriesClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.webhookDeliveries.<a href="/src/api/resources/caseManagement/resources/webhookDeliveries/client/Client.ts">getWebhookDelivery</a>({ ...params }) -> Paywise.WebhookDelivery</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Read-only webhook delivery log, plus manual redelivery.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.webhookDeliveries.getWebhookDelivery({
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.GetWebhookDeliveryRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WebhookDeliveriesClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.webhookDeliveries.<a href="/src/api/resources/caseManagement/resources/webhookDeliveries/client/Client.ts">redeliverWebhookDelivery</a>({ ...params }) -> Paywise.CaseWebhookCommandResult</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Read-only webhook delivery log, plus manual redelivery.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.webhookDeliveries.redeliverWebhookDelivery({
  'Idempotency-Key': 'Idempotency-Key',
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.RedeliverWebhookDeliveryRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WebhookDeliveriesClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## Webhooks

<details><summary><code>client.caseManagement.webhooks.<a href="/src/api/resources/caseManagement/resources/webhooks/client/Client.ts">listWebhooks</a>({ ...params }) -> core.Page&lt;Paywise.Webhook, Paywise.PaginatedWebhookList&gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Company-scoped webhook endpoint management.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse = await client.caseManagement.webhooks.listWebhooks();
for await (const item of pageableResponse) {
  console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.caseManagement.webhooks.listWebhooks();
while (page.hasNextPage()) {
  page = await page.getNextPage();
}

// You can also access the underlying response
const response = page.response;
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.ListWebhooksRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WebhooksClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.webhooks.<a href="/src/api/resources/caseManagement/resources/webhooks/client/Client.ts">createWebhook</a>({ ...params }) -> Paywise.CaseWebhookWithSecret</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Company-scoped webhook endpoint management.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.webhooks.createWebhook({
  'Idempotency-Key': 'Idempotency-Key',
  description: 'Primary integration webhook',
  enabled: true,
  events: ['mandate.created', 'payment.reported'],
  url: 'https://hooks.example.test/paywise',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.WebhookRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WebhooksClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.webhooks.<a href="/src/api/resources/caseManagement/resources/webhooks/client/Client.ts">getWebhook</a>({ ...params }) -> Paywise.Webhook</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Company-scoped webhook endpoint management.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.webhooks.getWebhook({
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.GetWebhookRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WebhooksClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.webhooks.<a href="/src/api/resources/caseManagement/resources/webhooks/client/Client.ts">deleteWebhook</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Company-scoped webhook endpoint management.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.webhooks.deleteWebhook({
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.DeleteWebhookRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WebhooksClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.webhooks.<a href="/src/api/resources/caseManagement/resources/webhooks/client/Client.ts">updateWebhook</a>({ ...params }) -> Paywise.Webhook</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Company-scoped webhook endpoint management.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.webhooks.updateWebhook({
  id: 'id',
  description: 'Primary integration webhook (now with statements)',
  events: ['mandate.created', 'payment.reported', 'statement.published'],
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.PatchedWebhookRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WebhooksClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.webhooks.<a href="/src/api/resources/caseManagement/resources/webhooks/client/Client.ts">rotateWebhookSecret</a>({ ...params }) -> Paywise.CaseWebhookWithSecret</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Company-scoped webhook endpoint management.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.webhooks.rotateWebhookSecret({
  'Idempotency-Key': 'Idempotency-Key',
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.RotateWebhookSecretRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WebhooksClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.caseManagement.webhooks.<a href="/src/api/resources/caseManagement/resources/webhooks/client/Client.ts">testWebhook</a>({ ...params }) -> Paywise.CaseWebhookCommandResult</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Company-scoped webhook endpoint management.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.caseManagement.webhooks.testWebhook({
  'Idempotency-Key': 'Idempotency-Key',
  id: 'id',
  event: 'payment.reported',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.caseManagement.CaseWebhookTestEventRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WebhooksClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## Companies

<details><summary><code>client.partner.companies.<a href="/src/api/resources/partner/resources/companies/client/Client.ts">listManagedCompanies</a>({ ...params }) -> core.Page&lt;Paywise.CompanyList, Paywise.PaginatedCompanyListList&gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List the companies this partner manages.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse = await client.partner.companies.listManagedCompanies();
for await (const item of pageableResponse) {
  console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.partner.companies.listManagedCompanies();
while (page.hasNextPage()) {
  page = await page.getNextPage();
}

// You can also access the underlying response
const response = page.response;
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.partner.ListManagedCompaniesRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CompaniesClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.partner.companies.<a href="/src/api/resources/partner/resources/companies/client/Client.ts">onboardACompany</a>({ ...params }) -> Paywise.CompanyCreateResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a company managed by this partner. Requires an `Idempotency-Key` header (a retry with the same key replays the original response without setup URLs). Requires the `partner:companies:write` scope. Select required `onboarding_mode` (`api_only` or `web_flow`). Missing mode returns 400 `onboarding_mode_required`; a mode without the exact live Partner entitlement returns 403 `onboarding_mode_not_allowed`.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.partner.companies.onboardACompany({
  'Idempotency-Key': 'Idempotency-Key',
  address: {
    city: 'Berlin',
    country: 'DE',
    postal_code: '10115',
    street: 'Example Avenue 5',
  },
  data_sharing_basis: 'self_authorized',
  default_claim_type: 'H11',
  external_reference: 'crm-4711',
  legal_form: 'gmbh',
  legal_representatives: [
    {
      name: 'Taylor Example',
      type: 'managing_director',
    },
  ],
  name: 'Example Manufacturing GmbH',
  notification_channels: [
    {
      notifications: ['requests_to_client', 'status_updates', 'statements'],
      type: 'email',
      value: 'operations@example.test',
    },
  ],
  onboarding_mode: 'api_only',
  payout_bank_account: {
    account_holder: 'Example Manufacturing GmbH',
    iban: 'DE89370400440532013000',
  },
  phone: '+49301234567',
  tax_treatment: 'input_tax_deductible',
  users: [
    {
      email: 'admin@example.test',
      first_name: 'Taylor',
      last_name: 'Example',
      role: 'admin',
      skip_email_verification: false,
    },
  ],
  vat_number: 'DE129273398',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.partner.CompanyCreateRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CompaniesClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.partner.companies.<a href="/src/api/resources/partner/resources/companies/client/Client.ts">getAManagedCompany</a>({ ...params }) -> Paywise.Company</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a single managed company by its uuid.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.partner.companies.getAManagedCompany({
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.partner.GetAManagedCompanyRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CompaniesClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.partner.companies.<a href="/src/api/resources/partner/resources/companies/client/Client.ts">updateACompanyPatch</a>({ ...params }) -> Paywise.Company</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Partially update a managed company. A company disconnected by this partner is inaccessible and returns `404 not_found`. An empty or unchanged PATCH is a no-op that leaves `updated_at` and the ETag untouched. Sending `onboarding_mode` returns 409 `onboarding_mode_immutable`.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.partner.companies.updateACompanyPatch({
  id: 'id',
  notification_channels: [
    {
      notifications: ['requests_to_client', 'status_updates', 'statements'],
      type: 'email',
      value: 'operations@example.test',
    },
  ],
  phone: '+49307654321',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.partner.PatchedCompanyRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CompaniesClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.partner.companies.<a href="/src/api/resources/partner/resources/companies/client/Client.ts">releaseACompany</a>({ ...params }) -> Paywise.CompanyReleaseReceipt</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

End all of this partner's access to a managed company. The company keeps its submitted cases, users, portal access and any credentials of its own. Orders this partner created on the company's behalf and never submitted are deleted; submitted orders and the company's own drafts survive. The company's `external_reference` is cleared so the same reference can onboard a fresh company later; the record itself stays attributed to the partner for history. Emits `company.access.revoked` with `reason: "partner_released"`. Requires an `Idempotency-Key` header and the `partner:companies:write` scope. Returns only an id and `case_access: unavailable` receipt. The same key replays this receipt; a new key after disconnection returns 404.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.partner.companies.releaseACompany({
  'Idempotency-Key': 'Idempotency-Key',
  id: 'id',
  reason: 'Client ended the partner engagement.',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.partner.CompanyReleaseRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CompaniesClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## Company users

<details><summary><code>client.partner.companyUsers.<a href="/src/api/resources/partner/resources/companyUsers/client/Client.ts">listCompanyMemberships</a>({ ...params }) -> core.Page&lt;Paywise.Membership, Paywise.PaginatedMembershipList&gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The memberships of one managed company: list, add, and revoke users.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse = await client.partner.companyUsers.listCompanyMemberships({
  company_id: 'company_id',
});
for await (const item of pageableResponse) {
  console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.partner.companyUsers.listCompanyMemberships({
  company_id: 'company_id',
});
while (page.hasNextPage()) {
  page = await page.getNextPage();
}

// You can also access the underlying response
const response = page.response;
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.partner.ListCompanyMembershipsRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CompanyUsersClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.partner.companyUsers.<a href="/src/api/resources/partner/resources/companyUsers/client/Client.ts">addACompanyMembership</a>({ ...params }) -> Paywise.MembershipWithSetupUrl</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The memberships of one managed company: list, add, and revoke users.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.partner.companyUsers.addACompanyMembership({
  'Idempotency-Key': 'Idempotency-Key',
  company_id: 'company_id',
  body: {
    email: 'email',
    first_name: 'first_name',
    last_name: 'last_name',
    role: 'admin',
  },
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.partner.AddACompanyMembershipRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CompanyUsersClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.partner.companyUsers.<a href="/src/api/resources/partner/resources/companyUsers/client/Client.ts">getACompanyMembership</a>({ ...params }) -> Paywise.Membership</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The memberships of one managed company: list, add, and revoke users.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.partner.companyUsers.getACompanyMembership({
  company_id: 'company_id',
  membership_id: 'membership_id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.partner.GetACompanyMembershipRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CompanyUsersClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.partner.companyUsers.<a href="/src/api/resources/partner/resources/companyUsers/client/Client.ts">changeAPendingMembershipRole</a>({ ...params }) -> Paywise.Membership</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The memberships of one managed company: list, add, and revoke users.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.partner.companyUsers.changeAPendingMembershipRole({
  company_id: 'company_id',
  membership_id: 'membership_id',
  role: 'admin',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.partner.MembershipRoleRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CompanyUsersClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.partner.companyUsers.<a href="/src/api/resources/partner/resources/companyUsers/client/Client.ts">cancelAPendingCompanyMembership</a>({ ...params }) -> Paywise.Membership</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The memberships of one managed company: list, add, and revoke users.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.partner.companyUsers.cancelAPendingCompanyMembership({
  'Idempotency-Key': 'Idempotency-Key',
  company_id: 'company_id',
  membership_id: 'membership_id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.partner.CancelAPendingCompanyMembershipRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CompanyUsersClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.partner.companyUsers.<a href="/src/api/resources/partner/resources/companyUsers/client/Client.ts">replaceAndResendAPendingSetupToken</a>({ ...params }) -> Paywise.MembershipWithSetupUrl</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The memberships of one managed company: list, add, and revoke users.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.partner.companyUsers.replaceAndResendAPendingSetupToken({
  'Idempotency-Key': 'Idempotency-Key',
  company_id: 'company_id',
  membership_id: 'membership_id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.partner.ReplaceAndResendAPendingSetupTokenRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CompanyUsersClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.partner.companyUsers.<a href="/src/api/resources/partner/resources/companyUsers/client/Client.ts">revokeAnActiveCompanyMembership</a>({ ...params }) -> Paywise.Membership</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The memberships of one managed company: list, add, and revoke users.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.partner.companyUsers.revokeAnActiveCompanyMembership({
  'Idempotency-Key': 'Idempotency-Key',
  company_id: 'company_id',
  membership_id: 'membership_id',
  reason: 'reason',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.partner.MembershipRevocationRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `CompanyUsersClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## Events

<details><summary><code>client.partner.events.<a href="/src/api/resources/partner/resources/events/client/Client.ts">listEvents</a>({ ...params }) -> core.Page&lt;Paywise.PartnerEventFeedEvent, Paywise.PartnerPaginatedEventFeed&gt;</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return one page of the partner's event feed, oldest first.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse = await client.partner.events.listEvents();
for await (const item of pageableResponse) {
  console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.partner.events.listEvents();
while (page.hasNextPage()) {
  page = await page.getNextPage();
}

// You can also access the underlying response
const response = page.response;
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.partner.ListEventsRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EventsClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## Meta

<details><summary><code>client.partner.meta.<a href="/src/api/resources/partner/resources/meta/client/Client.ts">healthCheck</a>() -> Paywise.PartnerHealthResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Unauthenticated liveness check for the Partner API.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.partner.meta.healthCheck();
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `MetaClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.partner.meta.<a href="/src/api/resources/partner/resources/meta/client/Client.ts">getPartnerTokenInfo</a>() -> Paywise.PartnerTokenInfoResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return non-PII metadata about the calling partner token: its id, name, scopes, capabilities and the owning partner. It never returns the owner's email or name.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.partner.meta.getPartnerTokenInfo();
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `MetaClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## Legal forms

<details><summary><code>client.partner.legalForms.<a href="/src/api/resources/partner/resources/legalForms/client/Client.ts">listLegalForms</a>({ ...params }) -> Paywise.LegalFormCatalog[]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return the authenticated, tenant-independent public catalog.

`representative_requirements` are the roles company readiness requires
for a company with the legal form, in the `legal_representatives[].type`
vocabulary. They can differ from the Case Management API's debtor catalog.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.partner.legalForms.listLegalForms();
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.partner.ListLegalFormsRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `LegalFormsClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## Usage

<details><summary><code>client.partner.usage.<a href="/src/api/resources/partner/resources/usage/client/Client.ts">getRateLimitHeadroom</a>() -> Paywise.UsageResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return an authoritative point-in-time snapshot of all rate-limit buckets applicable to the authenticated Partner credential. The call itself counts against the token and partner buckets. The snapshot also includes the hourly per-partner mail budgets `mail:company-create` (company creates) and `mail:membership-create` (membership invites, inline users included). Those two are charged only by successful commands.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.partner.usage.getRateLimitHeadroom();
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `UsageClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## Webhook deliveries

<details><summary><code>client.partner.webhookDeliveries.<a href="/src/api/resources/partner/resources/webhookDeliveries/client/Client.ts">listWebhookDeliveries</a>({ ...params }) -> core.Page&lt;Paywise.PartnerWebhookDelivery, Paywise.PaginatedPartnerWebhookDeliveryList&gt;</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse = await client.partner.webhookDeliveries.listWebhookDeliveries();
for await (const item of pageableResponse) {
  console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.partner.webhookDeliveries.listWebhookDeliveries();
while (page.hasNextPage()) {
  page = await page.getNextPage();
}

// You can also access the underlying response
const response = page.response;
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.partner.ListWebhookDeliveriesRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WebhookDeliveriesClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.partner.webhookDeliveries.<a href="/src/api/resources/partner/resources/webhookDeliveries/client/Client.ts">getWebhookDelivery</a>({ ...params }) -> Paywise.PartnerWebhookDelivery</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.partner.webhookDeliveries.getWebhookDelivery({
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.partner.GetWebhookDeliveryRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WebhookDeliveriesClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.partner.webhookDeliveries.<a href="/src/api/resources/partner/resources/webhookDeliveries/client/Client.ts">redeliverWebhookDelivery</a>({ ...params }) -> Paywise.PartnerWebhookCommandResult</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Re-enqueue a settled (`success`/`failed`) delivery as a new
attempt. 409 `conflict` on a disabled endpoint and 409
`delivery_in_progress` while the dispatcher still owns the row.
Deliveries outside current Partner authorization return 404.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.partner.webhookDeliveries.redeliverWebhookDelivery({
  'Idempotency-Key': 'Idempotency-Key',
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.partner.RedeliverWebhookDeliveryRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WebhookDeliveriesClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

## Webhooks

<details><summary><code>client.partner.webhooks.<a href="/src/api/resources/partner/resources/webhooks/client/Client.ts">listWebhooks</a>({ ...params }) -> core.Page&lt;Paywise.PartnerWebhook, Paywise.PaginatedPartnerWebhookList&gt;</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
const pageableResponse = await client.partner.webhooks.listWebhooks();
for await (const item of pageableResponse) {
  console.log(item);
}

// Or you can manually iterate page-by-page
let page = await client.partner.webhooks.listWebhooks();
while (page.hasNextPage()) {
  page = await page.getNextPage();
}

// You can also access the underlying response
const response = page.response;
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.partner.ListWebhooksRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WebhooksClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.partner.webhooks.<a href="/src/api/resources/partner/resources/webhooks/client/Client.ts">createWebhook</a>({ ...params }) -> Paywise.PartnerWebhookWithSecret</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.partner.webhooks.createWebhook({
  'Idempotency-Key': 'Idempotency-Key',
  url: 'url',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.partner.PartnerWebhookRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WebhooksClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.partner.webhooks.<a href="/src/api/resources/partner/resources/webhooks/client/Client.ts">getWebhook</a>({ ...params }) -> Paywise.PartnerWebhook</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.partner.webhooks.getWebhook({
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.partner.GetWebhookRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WebhooksClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.partner.webhooks.<a href="/src/api/resources/partner/resources/webhooks/client/Client.ts">deleteWebhook</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.partner.webhooks.deleteWebhook({
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.partner.DeleteWebhookRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WebhooksClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.partner.webhooks.<a href="/src/api/resources/partner/resources/webhooks/client/Client.ts">updateWebhook</a>({ ...params }) -> Paywise.PartnerWebhook</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.partner.webhooks.updateWebhook({
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.partner.PatchedPartnerWebhookRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WebhooksClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.partner.webhooks.<a href="/src/api/resources/partner/resources/webhooks/client/Client.ts">rotateWebhookSecret</a>({ ...params }) -> Paywise.PartnerWebhookWithSecret</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.partner.webhooks.rotateWebhookSecret({
  'Idempotency-Key': 'Idempotency-Key',
  id: 'id',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.partner.RotateWebhookSecretRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WebhooksClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>

<details><summary><code>client.partner.webhooks.<a href="/src/api/resources/partner/resources/webhooks/client/Client.ts">testWebhook</a>({ ...params }) -> Paywise.PartnerWebhookCommandResult</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.partner.webhooks.testWebhook({
  'Idempotency-Key': 'Idempotency-Key',
  id: 'id',
  event: 'company.created',
});
```

</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Paywise.partner.PartnerWebhookTestEventRequest`

</dd>
</dl>

<dl>
<dd>

**requestOptions:** `WebhooksClient.RequestOptions`

</dd>
</dl>
</dd>
</dl>

</dd>
</dl>
</details>
