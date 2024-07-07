# Description
The /update_author endpoint updates any specified attributes in a saved author profile.

# URL Structure

```
https://api.weaponizedword.org/analytics/1-0/update_author
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
    <td>author_id</td>
    <td>DEF456</td>
    <td>Yes if no client_id</td>
    <td>Alphanumeric</td>
  </tr>
  <tr>
    <td>client_id</td>
    <td>456DEF</td>
    <td>Yes if no author_id</td>
    <td>Alphanumeric</td>
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
  <tr>
    <td>language_id</td>
    <td>eng</td>
    <td>No</td>
    <td>3-character ISO 639-3 code</td>
  </tr>
  </tbody>
</table>

# Resultset
If the URL is successfully accepted by the API, the header will show 200 (success) and the response will contain a JSON result set.

If for whatever a reason an author profile has not been updated (e.g. the replacement attributes are identical to the original attributes), the output will be false rather than true.

```
"updated" : "true"
```
