## getInSkillProducts

Gets In-Skill Products based on user's context for the Skill.

### Request

`GET /v1/users/~current/skills/~current/inSkillProducts`

#### Request body structure

```json
{
  request body structure here ...
}
```

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
      <td markdown="span">`{name of the parameter}`</td>
      <td markdown="span">{Yes or No}</td>
      <td markdown="span">{description of the parameter}</td>
      <td markdown="span">{location of the parameter (Path or Body or Query, etc.)}</td>
      <td markdown="span">{type of the parameter (String or Boolean, etc.)}</td>
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
      <td markdown="span">`{HTTP status}`</td>
      <td markdown="span">{description of the error}</td>
    </tr>
  </tbody>
</table>
