### The following will show how to Install/Enable and Use Devel Kint Module.



##### First Step

###### By using interface
Click **Manage->Extend** then into the search bar type Devel. 
It will apear then check the following boxes :
 - Devel
 - Devel generate
 - Devel Kint

##### By using Drush
```{r, engine='bash', count_lines}
$ drush dl devel
$ drush en kint
```
###### By using Drupal Console
```{r, engine='bash', count_lines}
$ drupal module:download devel --latest
$ drupal module:install kint
```
 
##### How to use it
After installing Devel you can use **kint()** and **ksm()** They will print variables.
 - _kint()_ Prints everything at the top of the page. When viewing a printed variable, Kint also displays a stack trace just below the output. Kint can also be used in Twig templates. To print a variable, just add {{ kint(variable) }} into the template.
 - _ksm()_ Prints passed argument(s) to the 'message' area of the page/theme.

##### Finally if you wish the changes to take effect. You must clear the cache.

### [Go Back To Debugging INDEX](https://github.com/ovanesb/drupal/tree/master/Drupal8/Debugging)
