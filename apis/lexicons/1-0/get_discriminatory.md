# Description
The /get_discriminatory endpoint retrieves discriminatory terms from the database. Discriminatory terms are terms which specifically pertain to a recipient's nationality, ethnicity, religion, gender, sexual orientation, disability or class.

# URL Structure
```
https://api.weaponizedword.org/lexicons/1-0/get_discriminatory
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
  <tr>
    <td>is_about_nationality</td>
    <td>Y</td>
    <td>No</td>
    <td>Y or N</td>
  </tr>
  <tr>
    <td>is_about_ethnicity</td>
    <td>Y</td>
    <td>No</td>
    <td>Y or N</td>
  </tr>
  <tr>
    <td>is_about_religion</td>
    <td>Y</td>
    <td>No</td>
    <td>Y or N</td>
  </tr>
  <tr>
    <td>is_about_gender</td>
    <td>Y</td>
    <td>No</td>
    <td>Y or N</td>
  </tr>
  <tr>
    <td>is_about_orientation</td>
    <td>Y</td>
    <td>No</td>
    <td>Y or N</td>
  </tr>
  <tr>
    <td>is_about_disability</td>
    <td>Y</td>
    <td>No</td>
    <td>Y or N</td>
  </tr>
  <tr>
    <td>is_about_class</td>
    <td>Y</td>
    <td>No</td>
    <td>Y or N</td>
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
  "is_about_nationalities" : "Y",
  "nationalities" : {
    "United States",
    "France"
  },
  "is_about_ethnicities" : "N",
  "ethnicities" : {
  },
  "is_about_religions" : "N",
  "religions" : {
  },
  "is_about_gender" : "N",
  "genders" : {
  },
  "is_about_orientation" : "N",
  "orientations" : {
  },
  "is_about_disability" : "N",
  "is_about_class" : "N",
  "is_archaic" : "N",
  "offensiveness" : "Extremely offensive",
  "created_on" : "2020-01-01 12:00:00",
  "updated_on" : "2020-01-01 12:00:00"
}
```
