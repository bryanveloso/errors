# Errors

A compilation of possibly silly custom Apache error pages to replace those mundane ones that usually show up at the time of epic failure.

## Installation

This is tailored for my Webfaction usage, so the easiest way to use these files would be to throw the below lines into an `.htaccess` file. 

    ErrorDocument 400 /errors/400.html
    ErrorDocument 401 /errors/401.html
    ErrorDocument 403 /errors/403.html
    ErrorDocument 404 /errors/404.html
    ErrorDocument 405 /errors/405.html
    ErrorDocument 408 /errors/408.html
    ErrorDocument 415 /errors/415.html
    ErrorDocument 500 /errors/500.html
    ErrorDocument 501 /errors/501.html
    ErrorDocument 502 /errors/502.html
    ErrorDocument 503 /errors/503.html
    ErrorDocument 504 /errors/504.html
    ErrorDocument 505 /errors/505.html

Should work that way for any shared server environment, although slapping these in your `httpd.conf` might work just as well. 

To make things easier (on me), the error documents use SSI. So you can edit `/errors/ssi/header.html` and `/errors/ssi/footer.html` to suit your needs. There is a CSS file referenced to make the error pages pretty that pulls off of my S3 server, you can choose to use it or replace it with your own.

Finally, there is an `.htaccess` file that sits at the root of _this_ directory. In it, you should change the following from the defaults I have in place:
    
    SetEnv TZ America/Los_Angeles
    SetEnv SERVER_ADMIN servers@revyver.com
    
