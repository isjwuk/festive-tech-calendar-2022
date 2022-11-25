# festive-tech-calendar-2022
Resources to accompany my session titled **"Secure your website headers in time for Christmas"**.

> HTTP security headers are often overlooked when taking a website into production. In this session you'll learn how Santa improves the security of his Azure Web App by following a few simple steps. You will also discover how his elves leverage free-to-use tools to both validate the changes and ensure that functionality is not impacted. By the end of the session you should have all the information you need to start improving the security posture of your own web applications.
## Demo Site
* [site](./site) - Code for example site used in demo.
  * [site/index.html](site/index.html) - Original Index Page (demo 1)
  * [site/indexwithstyle.html](site/indexwithstyle.html) - Revised Index Page (demo 2)
  * [site/indexwithscript.html](site/indexwithscript.html) - Revised Index Page (demo 3)
  * [site/calendar.jpg](site/calendar.jpg) - Background Image (Festive Tech Calendar)
  * [site/snowflake.png](site/snowflake.png) - Snowflake Image
  * [site/scripts.js](site/scripts.js) - Javascript Script (demo 3)
  * [site/styles.css](site/styles.css) - Stylesheet (demo 3)

## Config File

An example ``.htaccess`` config file to set headers on Apache Httpd-based servers (e.g. Linux PHP 7.4 Web App)
```
Header set Content-Security-Policy "default-src 'self'; frame-ancestors 'self';"
Header set X-Content-Type-Options nosniff
Header set Feature-Policy "microphone none;"
Header set Permissions-Policy "geolocation=(self), microphone=()"
Header set Strict-Transport-Security "max-age=31536000; includeSubDomains"
Header set Referrer-Policy no-referrer
```

## Links
* [Recording of session](https://www.youtube.com/watch?v=F67rEHs0md0)
* [Festive Tech Calendar](https://festivetechcalendar.com/)

### Tools
* [securityheaders.com](https://securityheaders.com)
* [permissionspolicy.com](https://www.permissionspolicy.com/)

### Further Reading
* [OWASP Secure Headers Project](https://owasp.org/www-project-secure-headers/)
* [Mozilla.org HTTP Header Documentation](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers)
* [learn.microsoft.com Example PowerShell for Azure App Gateway Setup](https://learn.microsoft.com/en-us/azure/application-gateway/tutorial-ssl-powershell)
