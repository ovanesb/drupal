### How to delete field and its storage.


##### Add the following two methods to .docroot/profiles/custom/{project name}/{project name}.install

##### Example (1) [Tested]
```php
/**
 * Deleting field storage field_text.
 */
function norden_update_8005() {
    \Drupal::entityManager()
        ->getStorage('field_storage_config')
        ->load('node' . '.' . 'field_text');
}

/**
 * Deleting field field_keyword.
 */
function norden_update_8006() {
    \Drupal::entityManager()
        ->getStorage('field_config')
        ->load('node' . '.' . 'news' . '.' . 'field_text');
}
```

##### Example (2)
```php

use Drupal\field\Entity\FieldStorageConfig;
use Drupal\field\Entity\FieldConfig;


/**
 * Deleting field storage field_text.
 */
function norden_update_8005() {
    FieldStorageConfig::loadByName('entity_type', 'field_name')->delete();
}

/**
 * Deleting field field_keyword.
 */
function norden_update_8006() {
   FieldConfig::loadByName('entity_type', 'bundle', 'field_name')->delete();
}
```

##### Example (3)


### [Go Back To Hooks INDEX](https://github.com/ovanesb/drupal/tree/master/Drupal8/Hooks)