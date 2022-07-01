# Laravel_deployment


### create .htaccess in website main directory


          <IfModule mod_rewrite.c>
              DirectoryIndex index.php

              RewriteEngine On 
              RewriteRule ^$ public/index.php [L]
              RewriteRule ^((?!public/).*)$ public/$1 [L,NC]

          </IfModule>
          
          


### create .htaccess in Hosting main directory
          
          RewriteEngine On
          RewriteCond %{HTTP_HOST} engineeringcracks\.com [NC]
          RewriteCond %{SERVER_PORT} 80
          RewriteRule ^(.*)$ https://engineeringcracks.com/$1 [R,L]
