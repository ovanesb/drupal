### What hooks are used for



Hooks are one of the ways how that modules can interact with the other modules or Drupal core subsystems. 
Hooks are used for a variety of tasks including preprocessing variables for template files (hook_preprocess()), altering lists of information (hook_tokens_alter(), hook_views_data_alter()), and manipulating forms (hook_form_alter()) amongst other things.

A hook can be thought of as an event listener in the sense that an event triggers an action.
The event in Drupal, such as deleting a node, would trigger the hook "hook_node_delete". 
If your module implemented hook_node_delete, that function would run when a node deletion occurred. 
As an example, your function might be to decrease the count of the total number of nodes, so when a node was deleted, your function would be called and lower the count by 1.


### [Go Back To Hooks INDEX](https://github.com/ovanesb/drupal/tree/master/Drupal8/Hooks)