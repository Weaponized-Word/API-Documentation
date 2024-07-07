# Description
The /submit_post endpoint submits a piece of user-generated content to the database, which is then analyzed.

# URL Structure
```
https://api.weaponizedword.org/analytics/1-0/submit_post
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
    <td>post</td>
    <td></td>
    <td>Yes</td>
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
  <tr>
    <td>is_discriminary</td>
    <td>N</td>
    <td>No</td>
    <td>Y or N</td>
  </tr>
  <tr>
    <td>is_threatening</td>
    <td>N</td>
    <td>No</td>
    <td>Y or N</td>
  </tr>
  <tr>
    <td>is_derogatory</td>
    <td>N</td>
    <td>No</td>
    <td>Y or N</td>
  </tr>
  </tbody>
</table>

# Resultset
If the URL is successfully accepted by the API, the header will show 200 (success) and the response will contain a JSON result set.

```
"post_id" : "abc123"
```
