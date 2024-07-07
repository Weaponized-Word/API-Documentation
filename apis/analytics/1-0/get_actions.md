# Description
The /get_actions endpoint retrieves end-user activities. Actions are defined as descriptions of any user-initiated activity, from changing a password to flagging another user's content.

# URL Structure
```
https://api.weaponizedword.org/analytics/1-0/get_actions
```

# Input Parameters
<table>
  <thead>
  <tr>
    <th>Parameter</th>
    <th>Example</th>
    <th>Mandatory</th>
    <th>Notes</th>
  </tr>
  </thead>
  <tbody>
  <tr>
    <td>token</td>
    <td>ABC123</td>
    <td>Yes</td>
    <td></td>
  </tr>
  <tr>
    <td>page</td>
    <td>1</td>
    <td>No</td>
    <td>Defaults to 1 if not specified.</td>
  </tr>
  <tr>
    <td>project_id</td>
    <td>123abc</td>
    <td>Yes</td>
    <td>Alphanumeric</td>
  </tr>
  <tr>
    <td>year</td>
    <td>2020</td>
    <td>Yes</td>
    <td>Numeric</td>
  </tr>
  <tr>
    <td>author_id</td>
    <td>DEF456</td>
    <td>No</td>
    <td>Alphanumeric</td>
  </tr>
  <tr>
    <td>client_id</td>
    <td>456DEF</td>
    <td>No</td>
    <td>Alphanumeric</td>
  </tr>
  <tr>
    <td>country_id</td>
    <td>ca</td>
    <td>No</td>
    <td>2-character ISO 3166-2 code</td>
  </tr>
  </tbody>
</table>

# Resultset
If the URL is successfully accepted by the API, the header will show 200 (success) and the response will contain a JSON result set.

```
"actions" : {
  "action_id" : "abc123",
  "author_id" : "def456",
  "client_id" : "456def",
  "action" : "The user's email address was changed.",
  "occurred_on" : "2020-01-01 12:00:00",
  "country_id" : "us",
  "country" : "United States",
  "city" : "New York"
}
```
