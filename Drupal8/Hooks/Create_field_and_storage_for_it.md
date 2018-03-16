### How to create field storage and instance of it and add it to a bundle.


##### Add the following two methods to .docroot/profiles/custom/{project name}/{project name}.install

##### First we will need to use the following two classes in our file.
```php
use Drupal\field\Entity\FieldStorageConfig;
use Drupal\field\Entity\FieldConfig;
```

##### Create field storage.
 - _entity_type_ Its entity type will be paragraph.
 - _field_name_ That is name of the filed that we are going to create.
 - _type_ That is what type of the filed we need checkbox, drop-down, text aria and etc.
 - We can add as many specification as we wish. As example we can see any other .yml storage files.
  
```php
// Create field storage.
$config = FieldStorageConfig::create([
    'field_name' => 'field_body',
    'entity_type' => 'paragraph',
    'type' => 'text_long',
    'cardinality' => 1,
]);
$config->save();
```

##### Create an instance of the field and attach it to the paragraph bundle text.
```php
$storage = FieldConfig::create([
    'field_name' => 'field_body',
    'entity_type' => 'paragraph',
    'bundle' => 'text',
    'label' => 'Body',
]);
$storage->save();
```

##### Create another instance of the field and attach it to the paragraph bundle text_two.
```php
$storage = FieldConfig::create([
    'field_name' => 'field_body',
    'entity_type' => 'paragraph',
    'bundle' => 'text_two',
    'label' => 'Body',
]);
$storage->save();
```

### [Go Back To Hooks INDEX](https://github.com/ovanesb/drupal/tree/master/Drupal8/Hooks)