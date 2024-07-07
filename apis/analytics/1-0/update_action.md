# Description
The /update_action endpoint updates any specified attributes in a user-initiated activity.

# URL Structure
```
https://api.weaponizedword.org/analytics/1-0/update_action
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
    <td>project_id</td>
    <td>123abc</td>
    <td>Yes</td>
    <td>Alphanumeric</td>
  </tr>
  <tr>
    <td>year</td>
    <td>2020</td>
    <td>Yes</td>
    <td></td>
  </tr>
  <tr>
    <td>action_id</td>
    <td>123abc</td>
    <td>Yes</td>
    <td>Alphanumeric</td>
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
    <td>action</td>
    <td></td>
    <td>No</td>
    <td></td>
  </tr>
  <tr>
    <td>ip</td>
    <td>128.0.0.1</td>
    <td>No</td>
    <td></td>
  </tr>
  <tr>
    <td>user_agent</td>
    <td></td>
    <td>No</td>
    <td></td>
  </tr>
  <tr>
    <td>country_id</td>
    <td>ca</td>
    <td>No</td>
    <td>2-character ISO 3166-2 code</td>
  </tr>
  <tr>
    <td>city</td>
    <td>ca</td>
    <td>No</td>
    <td></td>
  </tr>
  </tbody>
</table>

# Resultset
If the URL is successfully accepted by the API, the header will show 200 (success) and the response will contain a JSON result set.

If for whatever a reason an action has not been updated (e.g. the replacement attributes are identical to the original attributes), the output will be false rather than true.

```
"updated" : "true"
```
