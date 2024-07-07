# Description
The /create_author endpoint creates an author profile in the database against which you can add posts and actions. Note that authors can have two unique identifiers: an author_id, which is assigned by The Weaponized Word, and a client_id, which represents the user's ID in your own system. Author_ID and client_id must both be unique; two authors cannot share the same author_id or client_id. In general, The Weaponized Word's website and API will reference the author_id rather than client_id, although both will be displayed (or can be used as input parameteres) where available.

# URL Structure
```
https://api.weaponizedword.org/analytics/1-0/create_author
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
    <td>client_id</td>
   <td>123abc</td>
    <td>No</td>
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

```
"author_id" : "abc123"
```
