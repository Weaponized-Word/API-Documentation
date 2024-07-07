# Description
The /analyze_post endpoint accepts a piece of user-generated content and returns information about that content, including whether it contains discriminatory or otherwise problematic language.

# URL Structure
```
https://api.weaponizedword.org/analytics/1-0/analyze_post
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
   <td>post</td>
   <td>This is a test post.</td>
   <td>Yes</td>
   <td>Alphanumeric</td>
  </tr>
  <tr>
   <td>language_id</td>
   <td>eng</td>
   <td>No</td>
   <td>3-character ISO 639-3 code</td>
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

Note that each probability result is accompanied with a version number. This represents the version number of the NLP classifier that was used to generate the result.

```
"analysis" : {
  "probability_discriminatory" : {
    "probability" : 0.00,
    "version" : 1.0
  }
  "probability_threatening" : {
    "probability" : 0.00,
    "version" : 1.0
  }
  "probability_derogatory" : {
    "probability" : 0.00,
    "version" : 1.0
  }
}
```
