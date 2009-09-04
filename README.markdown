# Errors

A compilation of possibly silly custom Apache error pages to replace those mundane ones that usually show up at the time of epic failure.

## Installation

This is tailored for my Webfaction usage, so the easiest way to use these files would be to throw the below lines into an `.htaccess` file. 

    ErrorDocument 301 /errors/301.html
    ErrorDocument 302 /errors/302.html
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