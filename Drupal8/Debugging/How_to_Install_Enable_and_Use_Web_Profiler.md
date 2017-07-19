### The following will show how to Install/Enable and Use Web Profiler Module.



##### First Step

###### By using interface
Click **Manage->Extend** then into the search bar type _Web Profiler_. 
It will apear then check the following boxes :
 - Web Profiler

##### By using Drush
```{r, engine='bash', count_lines}
$ drush dl devel
$ drush en webprofiler
```
###### By using Drupal Console
```{r, engine='bash', count_lines}
$ drupal module:download devel --latest
$ drupal module:install webprofiler
```
 
##### How to use it

##### Configuring Web Profiler
 - Web Profiler lets you navigate directly to the class and method by clicking it. It’ll open the configured IDE and go directly to the method. This makes it easy to get to the source with a single click. Go to the “Webprofiler settings” page (admin/config/development/devel/webprofiler) or click on the “Configure Webprofiler” link by hovering over the Drupal icon on the left. Click on the “IDE SETTINGS” field-set and add phpstorm://open?file=@file&line=@line into “IDE link”. It will do it for PhpStorm.

 - Displaying Timeline. For Web Profiler to display the details on the timeline page you must add the following two lines to your settings.php or settings.local.php.

```php
$class_loader->addPsr4('Drupal\\webprofiler\\', [ __DIR__ . '/../../modules/contrib/devel/webprofiler/src']);
$settings['container_base_class'] = '\Drupal\webprofiler\DependencyInjection\TraceableContainer';
``` 


**More [here](https://www.webwash.net/debug-site-performance-using-web-profiler-in-drupal-8/)**



##### Finally if you wish the changes to take effect. You must clear the cache.

### [Go Back To Debugging INDEX](https://github.com/ovanesb/drupal/tree/master/Drupal8/Debugging)

