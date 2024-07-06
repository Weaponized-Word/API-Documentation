# Current Versions
Please read this **entire page** before proceeding into the version-specific documentation.

- [Analytics v1.0](/apis/analytics/1-0.md)
- [Lexicons v1.0](/apis/lexicons/1-0.md)

Decimal increments are backwards-compatible. Integer increments are (generally) not. In other words, an integration built for v2.0 will work reliably with v2.1 (albeit without the extra features of 2.1) by simply changing the version number in the URL from 2.0 to 2.1 to avoid accessing the older deprecated version.

# How It Works
Multiple APIs are available, each of which allows for multiple endpoints. An API is queried with an API name, a version number, an endpoint (which defines the type of information requested) and a payload containing input parameters (sent by POST), and then returns a resultset.

The URL structure for querying the API is as follows:

```
https://api.weaponizedword.org/analytics/1-0/authenticate
```

In this example,

- "analytics" represents the desired API
- "1-0" represents the version number
- "authenticate" represents the endpoint

# Authentication Phase
Each API requires an authentication handshake prior to the actual query itself. The API key is obtained from your Weaponized Word account.

```
{
  api_key: ABC123
}
```

The returned data provides the input parameters which were queried, plus a resultset (in this case a session token), plus any warnings and/or errors:

```
{
  datetime: gmt_time,
  key: ABC123,
  format: json,
  result: [
    token: DEF456,
    expires_on: "2018-01-01 12:00:00"
  ]
  errors: [
    [789, "Incorrect key"]
  ]
  warnings:[
    [012, "Unspecified format"]
  ]
}
```

Note that this resultset is solely illustrative; a token would never be provided if there were errors, only warnings.

Tokens will expire within one hour of issue.

# Query Phase
The token provided in the authentication phase is used as an input parameter to authenticate phase two: the actual data query. The result set will look something like this:

```
{
  datetime: gmt_time,
  token: DEF456,
  expires_on: "2018-01-01 12:00:00",
  format: json,
  page: 1,
  total_pages: 14,
  result: [
  ]
  errors: [
  ]
  warnings:[
  ]
}
```

Again, this simple result set is solely illustrative; there is no need for empty key-value pairs.

# Troubleshooting Common Mistakes
If you're having trouble connecting after following our [quick-start tutorial](/tutorial/README.md), please check for the following common errors:

- Are you using the proper API and version number in all your URLs, e.g. api.weaponizedword.org / desired api / version-increment / authenticate ? Slightly old versions of the API deprecate but are still usable, while much older versions are retired and can no longer be queried.
- Are you using the "api." subdomain in your URLs?
- Are you remembering to send your query as a POST rather than a GET? POST is more secure, but some tools (like Postman) default to GET.
- Are you remembering to send your input parameters within the body of your query, rather than in the header?
- Are you authenticating before querying other endpoints?
- Are you remembering to re-authenticate after an hour?

# Daily Rate Limiting
Access to the APIs is limited by your plan's maximum daily query limit. It is strongly recommended that systems which connect with an API do not do so in user real-time. A safer architecture is to query data asynchronously and then implement locally for better performance and no redundant data retrieval.

# Acceptable Usage
Failing to respect the daily query limit, submitting duplicate queries, or repeatedly querying an API in user real-time are all prohibited by the Weaponized Word's [Terms of Use](https://weaponizedword.org/terms_of_use) and can result in users being banned temporarily or permanently, or receiving a lower query threshold. For assistance architecting a mutually performance-optimized data integration, please contact us.

# Understanding Problematic Responses
Please familiarize yourself with the Weaponized Word's [API error and warning codes](https://weaponizedword.org/api_error_codes), which are critical for letting you know what's wrong with a given query, whether you're getting close to your query limit or whether the version of the API you're accessing is deprecated and approaching retirement. Failing to implement appropriate error handling based on error codes can result in being banned from the API.

# Terms of Use
Your use of the APIs acknowledges your consent with the Weaponized Word's [Terms of Use](https://weaponizedword.org/terms_of_use).
