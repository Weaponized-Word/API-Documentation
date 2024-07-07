# Description
The /get_derogatory endpoint retrieves derogatry and otherwise insulting terms from the database. Derogatory terms are terms which are used as a general insult regardless of the recipient's group identity.

# URL Structure
```
https://api.weaponizedword.org/lexicons/1-0/get_derogatory
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
    <td>language_id</td>
    <td>eng</td>
    <td>Plan-dependent</td>
    <td>3-character ISO 639-3 code</td>
  </tr>
  </tbody>
</table>

# Resultset
If the URL is successfully accepted by the API, the header will show 200 (success) and the response will contain a JSON result set.

```
{
  "term" : "apples",
  "term_id" : "abc123",
  "variant_of" : "pears",
  "variant_of_id" : "def456",
  "plural_of" : "apple",
  "plural_of_id" : "ghi789",
  "romanization_of" : "",
  "romanization_of_id" : "",
  "language_id" : "eng",
  "language" : "English",
  "malignant_meaning" : "Bad fruit",
  "benign_meaning" : "Good fruit",
  "is_archaic" : "N",
  "offensiveness" : "Extremely offensive",
  "created_on" : "2020-01-01 12:00:00",
  "updated_on" : "2020-01-01 12:00:00"
}
```
