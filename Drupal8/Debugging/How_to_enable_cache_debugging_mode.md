### The following will enable cache debugging mode for drupal 8.


##### First Step
Navigate to sites/development.services.yml and add the following under parameters:
```{r, engine='bash', count_lines}
parameters:
  http.response.debug_cacheability_headers: true
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


### [Go Back To Debugging INDEX](https://github.com/ovanesb/drupal/tree/master/Drupal8/Debugging)
