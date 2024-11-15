# WordPress Notes

## Theme Folder Paths
1. `echo get_template_directory_uri();`  
   *Path of theme folder*

2. `bloginfo('template_directory');`  
   *Path to theme folder*

## Header and Footer
3. `get_header()`  
   *Call `header.php` file*

4. `get_footer()`  
   *Call `footer.php` file*

## Navigation Menus
5. `register_nav_menus()`  
   *Register menus in admin*

6. `wp_nav_menu()`  
   *Use to display menus*

## Title and URL
7. `the_title()`  
   *Displays the title of the current post/page*

8. `echo site_url()`  
   *Get the base URL (e.g., index.php after URL)*

---

## Content Display
*Use these functions in `page.php`*

9. `the_content()`  
   *Display the content of the current post/page*

10. `the_post()`  
    *Fetch data in the form of posts*

11. `echo get_the_content()`  
    *Display the content with additional processing*

---

## Thumbnail Support
*Add this in `functions.php` to enable thumbnails*

12. `add_theme_support('post-thumbnails');`

### Display Thumbnail Images
*Use these functions to display thumbnail images with or without parameters:*

1. `the_post_thumbnail();`  
   *Without parameters*

2. `the_post_thumbnail('thumbnail');`  
   *Thumbnail size (default 150px x 150px max)*

3. `the_post_thumbnail('medium');`  
   *Medium size (300px x 300px max)*

4. `the_post_thumbnail('large');`  
   *Large size (1024px x 1024px max)*

5. `the_post_thumbnail('full');`  
   *Full size (unmodified)*

6. `the_post_thumbnail(array(100,100));`  
   *Custom size (width, height)*

### Get Image Path
1. `wp_get_attachment_image_src(get_post_thumbnail_id(), 'large');`  
   *Retrieve the URL of a specific image size*

---

## Add Logo
*Enable custom logo support in `functions.php`*

1. `add_theme_support('custom-header');`

*Use in `header.php` to display the logo:*
`<?php $logoimage = get_header_image(); ?>`
*Use in src*
`src="<?php echo $logoimage;  ?>"`

---

## Custom Page Template
