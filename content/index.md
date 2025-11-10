---
title: Welcome to Quartz
---

This is a blank Quartz installation.
See the [documentation](https://quartz.jzhao.xyz) for how to get started.

Hosting options a) Immedaite, b). xamp c). Docker  d). hubpages

a). Immediate

if running other ports

 npx quartz build --serve --port 3000

b). xamp

1) copy   project --- public    to xamp\htdocs\quartzpublic

2) add .htaccess

--- code ---
RewriteEngine On
 
ErrorDocument 404 /404.html
 
# Rewrite rule for .html extension removal (with directory check)
RewriteCond %{REQUEST_FILENAME} !-f
RewriteCond %{REQUEST_FILENAME} !-d
RewriteCond %{DOCUMENT_ROOT}/%{REQUEST_URI}.html -f
RewriteRule ^(.*)$ $1.html [L]
 
# Handle directory requests explicitly
RewriteCond %{REQUEST_FILENAME} -d
RewriteRule ^(.*)/$ $1/index.html [L]

--- code ---

3).   http://localhost:8012/quartzpublic/

c).  to Docker

d). hubpages