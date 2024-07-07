# Description
The /get_authors endpoint retrieves multiple authors from the database. For more granular information on a specific author, try the /get_author_details endpoint.

#URL Structure
```
https://api.weaponizedword.org/analytics/1-0/get_authors
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
    <td>No</td>
    <td>Numeric</td>
  </tr>
  <tr>
    <td>country_id</td>
    <td>ca</td>
    <td>No</td>
    <td>2-character ISO 3166-2 code</td>
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

Note that if a year has not been specified, fields such as "total_posts_this_year" will not contain data.

```
"authors" : {
  "author_id" : "def456",
  "client_id" : "456def",
  "country_id" : "us",
  "country" : "United States",
  "city" : "New York",
  "language_id" : "eng",
  "language" : "English",
  "total_posts_this_year" : 0,
  "discriminatory_posts_this_year" : 0,
  "derogatory_posts_this_year" : 0,
  "threatening_posts_this_year" : 0,
  "created_on" : "2020-01-01 12:00:00",
  "updated_on" : "2020-01-01 12:00:00"
}
```
