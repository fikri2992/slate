# Errors

The Bannerbite API uses the following error codes:


Error Code | Meaning
---------- | -------
400 | Bad Request -- Your request is invalid.
401 | Unauthorized -- Your API key is wrong.
403 | Forbidden -- The bannerbite requested is hidden for administrators only.
404 | Not Found -- The specified bannerbite could not be found.
405 | Method Not Allowed -- You tried to access a bannerbite with an invalid method.
406 | Not Acceptable -- You requested a format that isn't json.
410 | Gone -- The bannerbite requested has been removed from our servers.
418 | I'm a teapot.
429 | Too Many Requests -- You're requesting too many bannerbites! Slow down!
500 | Internal Server Error -- We had a problem with our server. Try again later.
503 | Service Unavailable -- We're temporarily offline for maintenance. Please try again later.
