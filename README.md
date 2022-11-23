# festive-tech-calendar-2022
Resources to accompany my session titled "Secure your website headers in time for Christmas".

## Contents
* [site](./site) - Code for example site used in demo.
  * [site/index.html](site/index.html) - Original Index Page (demo 1)
  * [site/indexwithstyle.html](site/indexwithstyle.html) - Revised Index Page (demo 2)
  * [site/indexwithscript.html](site/indexwithscript.html) - Revised Index Page (demo 3)
  * [site/calendar.jpg](site/calendar.jpg) - Background Image (Festive Tech Calendar)
  * [site/snowflake.png](site/snowflake.png) - Snowflake Image
  * [site/scripts.js](site/scripts.js) - Javascript Script (demo 3)
  * [site/styles.css](site/styles.css) - Stylesheet (demo 3)
* Example config file to set headers:

``.htaccess`` for Apache Httpd-based servers (e.g. Linux PHP Web App)
```
Header set Content-Security-Policy "default-src 'self'; frame-ancestors 'self';"
Header set X-Content-Type-Options nosniff
Header set Feature-Policy "microphone none;"
Header set Permissions-Policy "geolocation=(self), microphone=()"
Header set Strict-Transport-Security "max-age=31536000; includeSubDomains"
Header set Referrer-Policy no-referrer
```

## Links
* Recording of session
* [Festive Tech Calendar](https://festivetechcalendar.com/)
### Tools
* [securityheaders.com](https://securityheaders.com)
* [permissionspolicy.com](https://www.permissionspolicy.com/)

### Further Reading
* [OWASP Secure Headers Project](https://owasp.org/www-project-secure-headers/)
* [Mozilla.org HTTP Header Documentation](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers)
* [learn.microsoft.com Example PowerShell for Azure App Gateway Setup](https://learn.microsoft.com/en-us/azure/application-gateway/tutorial-ssl-powershell)
