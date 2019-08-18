# Bootstrap_Menu_WordPress
Bootstrap4 Walker Menu For WordPress
Add the following to your functions.php file.
```php
<?php

// Include custom nav_walker
require_once('bootstrap_menu.php');

// Register WordPress nav menu
register_nav_menu('main', 'Main Menu');
```

Create your nav menu
```php
<?php
wp_nav_menu(
	array(
		'theme_location' => 'boot',
		'container_class' => 'collapse navbar-collapse',
		'container_id' => 'navbarSupportedContent',
		'menu_class' => 'navbar-nav mr-auto',
		'walker' => new Bootstrap_Menu()
		)
);
?>
```
For Reference
https://developer.wordpress.org/reference/functions/wp_nav_menu/
