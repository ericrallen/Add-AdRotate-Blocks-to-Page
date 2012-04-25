Add-AdRotate-Blocks-to-Page
===========================

Adds a options for dynamically adding AdRotate Blocks to WordPress pages.

What is it?
-----------

This is a plug-in that extends the functionality of the AdRotate plug-in by 
creating an options page in the WordPress admin area that allows adminitrators
to define specific sections that they want to allow AdRotate blocks to be placed
inside of.

After setting up an AdRotate Ad Block Position in the options page, users can
select a Block from a dropdown of all created Blocks when editing pages.

Why use it?
-----------

As a Theme developer, you can access the Blocks that a user wants to show up in
an Ad Block Position via custom post data.

The names of the Ad Block Positions that you define, become the custom post meta
key.

### For Example

Let's say on the options page I define one Ad Block Position called My Block Position.

So in a your page template:

    `//get post custom meta data
    $custom = get_post_custom($post->ID);
    //get AdRotate Block ID with position of My Block Position
    $ad_block_id = $custom['my_block_position'][0];`
    
Now, to display it in your template, use the built in AdRotate display functions.

    `echo adrotate_block($ad_block_id);`

Is that it?
-----------

Yes.

But feel free to tweak it to suit your needs.
    
    