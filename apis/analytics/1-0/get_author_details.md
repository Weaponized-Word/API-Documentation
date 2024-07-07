# Description
The /get_author_details endpoint retrieves a single author from the database and provides greater detail than the /get_authors endpoint.

# URL Structure
```
https://api.weaponizedword.org/analytics/1-0/get_author_details
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
    <td>year</td>
    <td>2020</td>
    <td>No</td>
    <td>Numeric</td>
  </tr>
  </tbody>
</table>

# Resultset
If the URL is successfully accepted by the API, the header will show 200 (success) and the response will contain a JSON result set.

Note that if a year has not been specified, fields such as "total_posts_this_year" will not contain data.

```
"author" : {
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
  "updated_on" : "2020-01-01 12:00:00",
  "most_recent_activities_this_year" : {
    "occurred_on" : "2020-01-01 12:00:00",
    "post_id" : "GHI789",
    "post" : "This is a test post.",
    "action_id" : "",
    "action" : "",
    "ip" : "128.0.0.0",
    "country_id" : "us",
    "country" : "United States",
    "city" : "New York",
    "is_discriminatory" : "N",
    "probability_discriminatory" : 0.00,
    "is_derogatory" : "N",
    "probability_derogatory" : 0.00,
    "is_threatening" : "N",
    "probability_threatening" : 0.00
  }
}
```
