---
created: 2024-06-23
tags: []
modified: 2024-09-03T15:48:58+02:00
---
 


```bash
# Database
mysqldump -u root -p wordpress > wordpress_db_$(date --iso-8601).sql
# Directory
tar -cvzf wordpress_$(date --iso-8601).tar.gz --exclude="*.wpress" wordpress
```

```bash
mkdir backup
cp wp-config.php .htaccess backup
cp -R wp-content backup
rm wp*.php .htaccess license.txt readme.html xmlrpc.php
rm -rf wp-admin wp-includes
cp backup/wp-config.php .
```