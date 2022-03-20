# Automatically-add-nofollow-attribute-for-external-links.
Automatically add nofollow attribute for external links.
// Add nofollow
function my_nofollow($content)
{
    return stripslashes(wp_rel_nofollow($content));
}
add_filter('the_content', 'my_nofollow');
