## getInSkillProducts

Gets In-Skill Products based on user's context for the Skill.

### Request

`GET /v1/users/~current/skills/~current/inSkillProducts`

#### Request parameters

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
      <th>Parameter</th>
      <th>Required</th>
      <th>Description</th>
      <th>Location</th>
      <th>Type</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td markdown="span">Authorization</td>
      <td markdown="span">Yes</td>
      <td markdown="span">access token used for authentication and authorization. This is passed to the user in the SPI call.</td>
      <td markdown="span">header</td>
      <td markdown="span">String</td>
    </tr>
    <tr>
      <td markdown="span">Accept-Language</td>
      <td markdown="span">Yes</td>
      <td markdown="span">aUser's locale/language in context.</td>
      <td markdown="span">header</td>
      <td markdown="span">String</td>
    </tr>
  </tbody>
</table>

### Response

`200`

#### Response body structure

```json
{
  "inSkillProducts": [
    {
      "productId": "foo",
      "referenceName": "foo",
      "name": "Friendly Name",
      "type": "SUBSCRIPTION",
      "summary": "Description of the product.",
      "entitled": "NOT_ENTITLED",
      "purchasable": "PURCHASABLE",
      "activeEntitlementCount": 0,
      "purchaseMode": "TEST"
    }
  ],
  "isTruncated": true,
  "nextToken": "foobar"
}
```

#### Response body fields

<table>
  <colgroup>
    <col width="25%" />
    <col width="45%" />
    <col width="15%" />
    <col width="15%" />
  </colgroup>
  <thead>
    <tr>
      <th>Field</th>
      <th>Description</th>
      <th>Location</th>
      <th>Type</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td markdown="span">inSkillProductsResponse</td>
      <td markdown="span">List of In-Skill Products</td>
      <td markdown="span">body</td>
      <td markdown="span">Array of inSkillProduct</td>
    </tr>
    <tr>
      <td markdown="span">isTruncated</td>
      <td markdown="span"></td>
      <td markdown="span">body</td>
      <td markdown="span">boolean</td>
    </tr>
      <tr>
      <td markdown="span">nextToken</td>
      <td markdown="span"></td>
      <td markdown="span"></td>
      <td markdown="span">String</td>
    </tr>
  </tbody>
</table>

#### Errors

An unsuccessful request returns one of the following errors:

<table>
  <colgroup>
    <col width="30%" />
    <col width="70%" />
  </colgroup>
  <thead>
    <tr>
      <th>Status</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td markdown="span">400</td>
      <td markdown="span">Invalid request</td>
    </tr>
        <tr>
      <td markdown="span">401</td>
      <td markdown="span">The authentication token is invalid or doesn't have access to make this request</td>
    </tr>
        <tr>
      <td markdown="span">500</td>
      <td markdown="span">Internal Server Error</td>
    </tr>
  </tbody>
</table>
