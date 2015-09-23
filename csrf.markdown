# CSRF

Everyone knows CSRF but the TLDR here is find sensitive functions and attempt to CSRF. Burps CSRF PoC is fast and easy for this.

Many sites will have CSRF protection, focus on CSRF bypass! Common bypasses:
- Remove CSRF token from request
- Remove CSRF token parameter value
- Add bad control chars to CSRF parameter value
- Use a second identical CSRF param
- Change POST to GET

￼Debasish Mandal wrote a python tool to automate finding CSRF bypasses called [Burpy] (https://github.com/debasishm89/burpy).
Step 1: Enable logging in Burp. Crawl a site with Burp completely executing all functions.
Step 2: Create a template...
￼
Or focus on pages without the token in Burp:
https://github.com/arvinddoraiswamy/mywebappscripts/blob/master/BurpExtensions/csrf_token_detect.py


CSRF Common Critical functions:

- Add / Upload file
- Password change
- Email change
- Transfer Money / Currency
- Delete File
- Profile edit
