# Description
The /delete_author endpoint completely removes a saved author profile and any related posts or actions. Please use this endpoint with caution. There is no undo.

# URL Structure
```
https://weaponizedword.org/analytics/1-0/delete_author
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
  </tbody>
</table>

# Resultset
If the URL is successfully accepted by the API, the header will show 200 (success) and the response will contain a JSON result set.

If for whatever a reason an author profile has not been deleted (e.g. the author has already been deleted), the output will be false rather than true.

```
"updated" : "true"
```
