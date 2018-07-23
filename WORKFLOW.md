## create project
composer create-project drupal-composer/drupal-project:8.x-dev drupal --stability dev --no-interaction


## go into the created project folder
cd drupal

## install dependencies
composer install

## install cgr
composer global require consolidation/cgr 

## install drush
cgr drush/drush

## create db
mysql

## extra commands

### export configuration 
drush cex -y

### Apply database updates : go to /update.php

### Import configuration : /admin/config/development/configuration, review all changes make sense/are expected, then click `Import All`

### Clear caches : /admin/config/development/performance, then click `Clear All Caches`

https://github.com/consolidation/cgr#installation-and-usage
https://medium.com/@ChandeepKhosa/drupal-8-development-deployment-a-step-by-step-guide-7837cfae7924