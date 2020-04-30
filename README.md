=== DESCRIPTION  ===
  You don't need this module unless you're either a developer or another module you're using depends on it.

  Currently, both Drupal and Backdrop do not offer any hooks to do actions after an entity is inserted,
  updated, or deleted in the database. This module adds several new hooks to overcome this limitation:

  - hook_entity_postsave
  - hook_entity_postinsert
  - hook_entity_postupdate
  - hook_entity_postdelete
  - hook_node_postsave
  - hook_node_postinsert
  - hook_node_postupdate
  - hook_node_postdelete

=== INSTALLATION ===
  Install and enable the module as usual: https://backdropcms.org/user-guide/modules

=== USAGE ===
  Please read the hook_post_action.api file.

  If you want to quickly see it working, you can enable the bundled module hook_post_action_example,
  add/delete/update some contents and visit logs admin/reports/dblog

  WARNING: The _postsave, _postinsert and _postupdate hooks are also called when the entity is deleted,
  as there is no way to find out whether the entity/node is actually saved/inserted/updated.
  However, the module only calls the delete hooks when the entity is actually deleted from database.

AUTHORS AND MAINTAINERS
=======================
  Sina Salek http://sina.salek.ws

BACKDROP PORT
=======================
  Ryan Osītis https://ryanositis.com
