### The following will enable twig debugging mode for drupal 8.

##### When view source it will tell which template is where. Also shows where it starts and where it finishes


##### First Step
Navigate to sites/development.services.yml and add the following under parameters:
```{r, engine='bash', count_lines}
  twig.config:
    debug: true
```



##### Second Step
Change the permission of this sites/default/settings.local.php file like:
```{r, engine='bash', count_lines}
 $ sudo chmode 755 sites/default/settings.local.php
```

Then edit the sites/default/settings.local.php file and make sure the following is uncommented:
```php
/**
 * Enable local development services.
 */
$settings['container_yamls'][] = DRUPAL_ROOT . '/sites/development.services.yml';
```



##### Finally if you wish the changes to take effect. You must clear the cache.
