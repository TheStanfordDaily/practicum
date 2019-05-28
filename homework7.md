---
layout: default
title: Homework 7
nav: project
---

## Homework 7
Create a custom post type!

How to create a custom post type:
- Create a plugin: make the file `wp-content/plugins/tsd-movies/tsd-movies.php`
- Add the following to the plugin file (replace with plugin name):
```php
<?php
/*
 * Plugin Name: Ashwin's Plugin
 * Plugin URI: http://google.com
 * Description: First plugin
 * Version: 0.1
 * Author: Ashwin
 */

    // PHP Code here

 ?>
```
- Add a function to create the post type such as:
```php
function tsd_test_create_posttype() {
    register_post_type( 'movies',
    // CPT Options
            array(
                'labels' => array(
                    'name' => __( 'Movies' ),
                    'singular_name' => __( 'Movie' )
                ),
                	
                'taxonomies'  => array( 'tsd_movie_category' ),
                'public' => true,
                'has_archive' => true,
                'rewrite' => array('slug' => 'movies')
            )
        );
    }
// Hooking up our function to theme setup
add_action( 'init', 'tsd_test_create_posttype' );
```
- Go to http://localhost.stanforddaily.com/wp-admin/, go to the Plugins menu, then enable the Plugin.
- There should now be a menu item with "Movie" (or the custom post type) and you should be able to add/remove items!

<br><br>

| People    | Project Name  | Description | Links |
| ------- | ------ | ------- | ---- |
| Grace, Devansh | Jobs | Create jobs custom post type to connect with jobs board. | |
| Sunnie | Podcasts | Create "podcasts" custom post type. | |
| Cathy, Emily | Open Data | Create "dataset" custom post type to use with the open data project. | |