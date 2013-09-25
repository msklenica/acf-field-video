# ACF Video Field/s #
Contributors: jconroy    
Tags: acf, video, youtube, vimeo, custom field   
Requires at least: 3.6  
Tested up to: 3.6.1  
Stable tag: 1.0

Adds a 'video' field type for the [Advanced Custom Fields](http://wordpress.org/extend/plugins/advanced-custom-fields/) WordPress plugin.

## Description ##

Adds a 'video' field type for the [Advanced Custom Fields](http://wordpress.org/extend/plugins/advanced-custom-fields/) WordPress plugin.

## Compatibility ##

This add-on will work with:

* version 4 and up of ACF

## Installation ##

This add-on can be treated as both a WP plugin and a theme include.

**Install as Plugin**

1. Copy the 'acf-field-video' folder into your plugins folder
2. Activate the plugin via the Plugins admin page

**Include within theme**

1.	Copy the 'acf-field-video' folder into your theme folder (can use sub folders). You can place the folder anywhere inside the 'wp-content' directory
2.	Edit your functions.php file and add the code below (Make sure the path is correct to include the acf-video.php file)

```
php
add_action('acf/register_fields', 'my_register_fields');

function my_register_fields()
{
	include_once('acf-field-video/acf-video.php');
}
```

## Usage ##

1. Add a new field with a Field Type of "Video".
2. Set how you would like to preview the video e.g. Embed the video, show the video thumbnail (pulled from YouTube or Vimeo) or don't show a preview
3. Set how you would like to return the video/field when the field is called using functions like ```get_field()```  e.g. Return the video url, the thumbnail url, the embed code for the video or an array of all of these 
4. Publish the field / group as per ACF standard use.

**Retrieve Video**

1. Retrieve the video by using standard ACF functions for obtaining field values.


## Changelog ##

### 1.0 ###
* Initial release