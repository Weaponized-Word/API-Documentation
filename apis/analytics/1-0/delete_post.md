# Description
The /delete_post endpoint completely removes a saved post. Please use this endpoint with caution. There is no undo.

# URL Structure
```
https://api.weaponizedword.org/analytics/1-0/delete_post
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
    <td>post_id</td>
    <td>123abc</td>
    <td>Yes</td>
    <td>Alphanumeric</td>
  </tr>
  </tbody>
</table>

# Resultset
If the URL is successfully accepted by the API, the header will show 200 (success) and the response will contain a JSON result set.

If for whatever a reason a post has not been deleted (e.g. the post has already been deleted), the output will be false rather than true.

```
"updated" : "true"
```
