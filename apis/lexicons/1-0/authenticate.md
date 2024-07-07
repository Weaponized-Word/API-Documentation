# Description
The /authenticate endpoint is required to initiate an API session, and outputs a session token which is used for additional queries over the span of an hour. Once a session token has expired, a new one must be requested by using the /authenticate endpoint.

#URL Structure
```
https://api.weaponizedword.org/lexicons/1-0/authenticate
```

# Input Parameters</h3>
<table>
  <thead>
  <tr>
    <th><b>Parameter</b></th>
    <th><b>Example</b></th>
    <th><b><b>Mandatory</b></b></th>
  </tr>
  </thead>
  <tbody>
  <tr>
    <td>api_key</td>
    <td>ABC123</td>
    <td>Yes</td>
  </tr>
  </tbody>
</table>

# Resultset
<table>
  <thead>
  <tr>
    <th>Field</th>
    <th>Value</th>
    <th>Notes</th>
  </tr>
  </thead>
  <tbody>
  <tr>
    <td>token</td>
    <td>ABC123</td>
    <td></td>
  </tr>
  <tr>
    <td>requested_on</td>
    <td>2018-01-01 12:00:00</td>
    <td>GMT</td>
  </tr>
  <tr>
    <td>expires_on</td>
    <td>2018-01-01 13:00:00</td>
    <td>GMT</td>
  </tr>
  </tbody>
</table>
