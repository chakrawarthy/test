## Operation title

{description of the operation}

### Request

`{HTTP method} {HTTP path}`

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

`{HTTP status}`

#### Response body structure

```json
{
  response body structure here ...
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
      <td markdown="span">`{name of the field}`</td>
      <td markdown="span">{description of the field}</td>
      <td markdown="span">{location of the field (body or HTTP header, etc.)}</td>
      <td markdown="span">{type of the field (String or Boolean, etc.)}</td>
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
