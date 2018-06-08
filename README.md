# Removing-file-extensions-using-htaccess
To remove .php, .html, .htm extensions using .htaccess

- An `.htaccess` file is a simple ASCII file that you create with a text editor like Notepad or TextMate. It provides a way to make configuration changes on a per-directory basis.
 
 # With an .htaccess file you can:
 
- Redirect the user to different page
- Password protect a specific directory
- Block users by IP
- Preventing hot linking of your images
- Rewrite URIs
- Specify your own Error Documents

# Removing .php Extension from URL

 - RewriteEngine on
 - RewriteCond %{THE_REQUEST} /([^.]+)\.php [NC]
 - RewriteRule ^ /%1 [NC,L,R]

 - RewriteCond %{REQUEST_FILENAME}.php -f
 - RewriteRule ^ %{REQUEST_URI}.php [NC,L] 
 
 # Removing .html Extension from URL
 
- RewriteEngine on
- RewriteCond %{THE_REQUEST} /([^.]+)\.html [NC]
- RewriteRule ^ /%1 [NC,L,R]

- RewriteCond %{REQUEST_FILENAME}.html -f
- RewriteRule ^ %{REQUEST_URI}.html [NC,L]


 
- If you’re worried that search engines might index these pages as duplicate content, add a canonical meta tag in your HTML head:
 
