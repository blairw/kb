---
Title: bash
---

*&larr; back to [DevOps](?devops)*

# Apache HTTP Server

Available for [Linux](%base_url%/?devops/linux), [Mac](%base_url%/?devops/mac), and [Windows](%base_url%/?devops/windows) if using XAMPP.

## Username and password security

1. Modify your .htaccess to have the following rule:

    ```
    AuthType Basic
    AuthName "Password Protected Area"
    AuthUserFile /Library/WebServer/Documents/kittenhouse/.htpasswd
    Require valid-user
    ```

    ... where `/Library/WebServer/Documents/kittenhouse` is the path to your web app.

2. Execute this command to generate the appropriate `.htpasswd` file:

    `htpasswd -nb jeanvaljean onedaymore >> .htpasswd`

Sources for this section:
- [kremalicious](https://kremalicious.com/how-to-quickly-generate-encrypted-logins-on-a-mac-for-htaccess-protected-sites/)
- [htaccesstools.com](www.htaccesstools.com/articles/password-protection/)

## Force redirect to HTTPS

Put this in your `.htaccess`:

```
<IfModule mod_rewrite.c>
    ...

    RewriteEngine On
    RewriteCond %{HTTPS} off
    RewriteCond !%{HTTP_HOST} ^localhost$
    RewriteRule ^(.*)$ https://%{HTTP_HOST}%{REQUEST_URI} [L,R=301]
    
    ...
</IfModule>
```

The line `RewriteCond !%{HTTP_HOST} ^localhost$` is to disable the HTTPS-switching for your local web server (e.g. [apache](%base_url%/?devops/apache)). Remove that line if you don't need it.