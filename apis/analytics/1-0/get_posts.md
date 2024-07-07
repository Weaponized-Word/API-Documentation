# Description
The /get_posts endpoint retrieves end-user posts with available metadata. Posts are defined as pieces of user-generated content.

# URL Structure
```
https://api.weaponizedword.org/analytics/1-0/get_posts
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
  <tr>
    <td>is_discriminary</td>
    <td>false</td>
    <td>No</td>
    <td>True or false</td>
  </tr>
  <tr>
    <td>is_threatening</td>
    <td>false</td>
    <td>No</td>
    <td>True or false</td>
  </tr>
  <tr>
    <td>is_derogatory</td>
    <td>false</td>
    <td>No</td>
    <td>True or false</td>
  </tr>
  <tr>
    <td>is_fraudulent</td>
    <td>false</td>
    <td>No</td>
    <td>True or false</td>
  </tr>
  <tr>
    <td>is_disinformation</td>
    <td>false</td>
    <td>No</td>
    <td>True or false</td>
  </tr>
  </tbody>
</table>

# Resultset
If the URL is successfully accepted by the API, the header will show 200 (success) and the response will contain a JSON result set.

Note that fields such as "is_discriminatory" reflect data provided by the client, whereas "probability_descriminatory" reflect an assessment made by the Weaponized Word in the absence of client determination.

```
"posts" : {
  "post_id" : "def456",
  "author_id" : "456def",
  "client_id" : "123abc",
  "post" : "This is a test post.",
  "occurred_on" : "2020-01-01 12:00:00",
  "country_id" : "us",
  "country" : "United States",
  "city" : "New York",
  "is_discriminatory" : 0,
  "probability_discriminatory" : 0.00,
  "is_threatening" : 0,
  "probability_threatening" : 0.00,
  "is_derogatory" : 0,
  "probability_derogatory" : 0.00
}
```
