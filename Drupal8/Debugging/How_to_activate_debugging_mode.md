The following will enable the debugging mode for drupal 8.



First Step
```{r, engine='bash', count_lines}
$ sudo cp sites/example.settings.local.php sites/default/settings.local.php
$ sudo chmod 755 sites/default/settings.local.php
$ sudo chmod 755 sites/default/settings.php
$ sudo chmod 755 sites/default 
```


Second Step
Edit the settings.php file :
```{r, engine='bash', count_lines} 
$ vim sites/default/settings.php
```
Then uncommnet the following
```php
 if (file_exists($app_root . '/' . $site_path . '/settings.local.php')) {
   include $app_root . '/' . $site_path . '/settings.local.php';
 }
```
