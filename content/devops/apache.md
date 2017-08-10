---
Title: bash
---

*&larr; back to [DevOps](?devops)*

# Apache HTTP Server

Available for [Linux](%base_url%/?devops/linux), [Mac](%base_url%/?devops/mac), and [Windows](%base_url%/?devops/windows) if using XAMPP.

## Force redirect to HTTPS

Put this in your `.htaccess`:

```
<IfModule mod_rewrite.c>
    ...

    RewriteEngine On
    RewriteCond %{HTTPS} off
    RewriteRule ^(.*)$ https://%{HTTP_HOST}%{REQUEST_URI} [L,R=301]
    
    ...
</IfModule>
```