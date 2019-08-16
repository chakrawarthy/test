## /v1/users/~current/skills/~current/inSkillProducts

Gets In-Skill Products based on user's context for the Skill.

### Request
#### HTTP method and URL path
```http
GET /v1/users/~current/skills/~current/inSkillProducts
```

#### Request body structure
#### Request Parameters

<table>
<colgroup>
<col width="20%" />
<col width="15%" />
<col width="35%" />
<col width="15%" />
<col width="15%" />
</colgroup>
<thead>
<tr>
<th>Name</th>
<th>Located in</th>
<th>Description</th>
<th>Required</th>
<th>Schema</th>
</tr>
</thead>
<tbody>
<tr>
<td markdown="span">Accept-Language</td>
<td markdown="span">header</td>
<td markdown="span">User's locale/language in context</td>
<td markdown="span">yes</td>
<td markdown="span">string</td>
</tr>
<tr>
<td markdown="span">purchasable</td>
<td markdown="span">query</td>
<td markdown="span">Filter products based on whether they are purchasable by the user or not. * 'PURCHASABLE' - Products that are purchasable by the user. * 'NOT_PURCHASABLE' - Products that are not purchasable by the user.</td>
<td markdown="span">no</td>
<td markdown="span">string</td>
</tr>
<tr>
<td markdown="span">entitled</td>
<td markdown="span">query</td>
<td markdown="span">Filter products based on whether they are entitled to the user or not. * 'ENTITLED' - Products that the user is entitled to. * 'NOT_ENTITLED' - Products that the user is not entitled to.</td>
<td markdown="span">no</td>
<td markdown="span">string</td>
</tr>
<tr>
<td markdown="span">productType</td>
<td markdown="span">query</td>
<td markdown="span">Product type. * 'SUBSCRIPTION' - Once purchased, customers will own the content for the subscription period. * 'ENTITLEMENT' - Once purchased, customers will own the content forever. * 'CONSUMABLE' - Once purchased, customers will be entitled to the content until it is consumed. It can also be re-purchased.</td>
<td markdown="span">no</td>
<td markdown="span">string</td>
</tr>
<tr>
<td markdown="span">nextToken</td>
<td markdown="span">query</td>
<td markdown="span">When response to this API call is truncated (that is, isTruncated response element value is true), the response also includes the nextToken element, the value of which can be used in the next request as the continuation-token to list the next set of objects. The continuation token is an opaque value that In-Skill Products API understands. Token has expiry of 24 hours.</td>
<td markdown="span">no</td>
<td markdown="span">string</td>
</tr>
<tr>
<td markdown="span">maxResults</td>
<td markdown="span">query</td>
<td markdown="span">
  
sets the maximum number of results returned in the response body. If you want to retrieve fewer than upper limit of 100 results, you can add this parameter to your request. maxResults should not exceed the upper limit. The response might contain fewer results than maxResults, but it will never contain more. If there are additional results that satisfy the search `criteria`, but these results were not returned because maxResults was exceeded, the response contains isTruncated = true.
  
</td>
<td markdown="span">no</td>
<td markdown="span">number</td>
</tr>
</tbody>
</table>

### Response
#### Response body structure

<table>
<colgroup>
<col width="25%" />
<col width="45%" />
<col width="30%" />
</colgroup>
<thead>
<tr>
<th>Code</th>
<th>Description</th>
<th>Schema</th>
</tr>
</thead>
<tbody>
<tr>
<td markdown="span">200</td>
<td markdown="span">Returns a list of In-Skill products on success.</td>
<td markdown="span">
  
[InSkillProductsResponse](#servicesmonetizationinskillproduct)

</td>
</tr>
<tr>
<td markdown="span">400</td>
<td markdown="span">Invalid request</td>
<td markdown="span">
#/components/schemas/services.monetization.Error
</td>
</tr>
<tr>
<td markdown="span">401</td>
<td markdown="span">The authentication token is invalid or doesn't have access to make this request</td>
<td markdown="span">
#/components/schemas/services.monetization.Error
</td>
</tr>
<tr>
<td markdown="span">500</td>
<td markdown="span">Internal Server Error</td>
<td markdown="span">
#/components/schemas/services.monetization.Error
</td>
</tr>
</tbody>
</table>


## Type Schemas
### services.monetization.Error
#### Response body structure

<table>
<colgroup>
<col width="25%" />
<col width="15%" />
<col width="45%" />
<col width="15%" />
</colgroup>
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
<th>Required</th>
</tr>
</thead>
<tbody>
<tr>
<td markdown="span">message</td>
<td markdown="span">string</td>
<td markdown="span">Readable description of error</td>
<td markdown="span">no</td>
</tr>
</tbody>
</table>

### services.monetization.InSkillProductsResponse
#### Response body structure

<table>
<colgroup>
<col width="25%" />
<col width="15%" />
<col width="45%" />
<col width="15%" />
</colgroup>
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
<th>Required</th>
</tr>
</thead>
<tbody>
<tr>
<td markdown="span">inSkillProducts</td>
<td markdown="span">array</td>
<td markdown="span">List of In-Skill Products</td>
<td markdown="span">yes</td>
</tr>
<tr>
<td markdown="span">isTruncated</td>
<td markdown="span">boolean</td>
<td markdown="span"></td>
<td markdown="span">yes</td>
</tr>
<tr>
<td markdown="span">nextToken</td>
<td markdown="span">string</td>
<td markdown="span"></td>
<td markdown="span">yes</td>
</tr>
</tbody>
</table>

### services.monetization.InSkillProduct [MultiMarkdownOverview]
#### Response body structure

<table>
<colgroup>
<col width="25%" />
<col width="15%" />
<col width="45%" />
<col width="15%" />
</colgroup>
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
<th>Required</th>
</tr>
</thead>
<tbody>
<tr>
<td markdown="span">productId</td>
<td markdown="span">string</td>
<td markdown="span">Product Id</td>
<td markdown="span">yes</td>
</tr>
<tr>
<td markdown="span">referenceName</td>
<td markdown="span">string</td>
<td markdown="span">Developer selected in-skill product name. This is for developer reference only.</td>
<td markdown="span">yes</td>
</tr>
<tr>
<td markdown="span">name</td>
<td markdown="span">string</td>
<td markdown="span">Name of the product in the language from the "Accept-Language" header</td>
<td markdown="span">yes</td>
</tr>
<tr>
<td markdown="span">type</td>
<td markdown="span"></td>
<td markdown="span"></td>
<td markdown="span">yes</td>
</tr>
<tr>
<td markdown="span">summary</td>
<td markdown="span">string</td>
<td markdown="span">Product summary in the language from the "Accept-Language" header</td>
<td markdown="span">yes</td>
</tr>
<tr>
<td markdown="span">purchasable</td>
<td markdown="span"></td>
<td markdown="span"></td>
<td markdown="span">yes</td>
</tr>
<tr>
<td markdown="span">entitled</td>
<td markdown="span"></td>
<td markdown="span"></td>
<td markdown="span">yes</td>
</tr>
<tr>
<td markdown="span">entitlementReason</td>
<td markdown="span"></td>
<td markdown="span"></td>
<td markdown="span">yes</td>
</tr>
<tr>
<td markdown="span">activeEntitlementCount</td>
<td markdown="span">integer</td>
<td markdown="span">Total active purchases of the product made by the user. Note - For ENTITLEMENT and SUBSCRIPTION product types, the value is either zero(NOT_ENTITLED) or one(ENTITLED). For CONSUMABLE product type the value is zero or more, as CONSUMABLE can be re-purchased.</td>
<td markdown="span">yes</td>
</tr>
<tr>
<td markdown="span">purchaseMode</td>
<td markdown="span"></td>
<td markdown="span"></td>
<td markdown="span">yes</td>
</tr>
<tr>
<td markdown="span">startTime</td>
<td markdown="span">string</td>
<td markdown="span">For SUBSCRIPTION product types, this is the time when the valid subscription period starts.</td>
<td markdown="span">no</td>
</tr>
<tr>
<td markdown="span">endTime</td>
<td markdown="span">string</td>
<td markdown="span">For SUBSCRIPTION product types, this is the time when the valid subscription period ends.</td>
<td markdown="span">no</td>
</tr>
<tr>
<td markdown="span">subscriptionId</td>
<td markdown="span">string</td>
<td markdown="span">For SUBSCRIPTION product types, this is an identifier for a subscription which does not change with renewals or cancellations.</td>
<td markdown="span">no</td>
</tr>
</tbody>
</table>
