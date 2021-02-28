
## Installation
#### Dev Environment
```
git clone https://github.com/AkashAdarsh/StegOnline.git
cd StegOnline
(sudo) npm install -g @angular/cli
(sudo) npm install -i
(sudo) ng serve --open
```
#### Live Environment (Apache2)
This will install into the StegOnline/ folder of your site
```
cd ~/Documents #Or wherever you want to store it
git clone https://github.com/AkashAdarsh/StegOnline.git
cd StegOnline
(sudo) npm install -g @angular/cli
(sudo) npm install -i
(sudo) ng build --prod --base-href=/StegOnline/ --aot=false --build-optimizer=false --output-path=/var/www/html/StegOnline
```
Inside of the newly created /var/www/html/StegOnline folder, create the following .htaccess file:
```
Options +FollowSymLinks
RewriteCond %{REQUEST_FILENAME} !-f
RewriteRule ^(.*)$ index.html [L,QSA]
```
