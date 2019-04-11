# pico-jonbeckett

A simple theme for the [Pico](http://picocms.org/) CMS using [BootStrap](http://getbootstrap.com).

### Installation Instructions

* Copy the contents of the theme folder into the "themes" folder of your Pico installation.
* Edit the /config/config.php file of your Pico install as follows: <code>$config['theme'] = 'pico-jonbeckett';</code>

### Notes

* If you want to make a blog, create a folder within /content, and put your posts in it (purely to keep them organised - they are actually picked up by the blog page by having dates). For each post, use the template "post", and make sure they have a date metadata property. Then make a content file in the root of /content with the template "blog", and it will list all pages it finds that have a date in their metadata, in reverse order.
* The blog template has Disqus built-in. If you want to use it, add <code>$config["disqus"]="username";</code> to the config file, and use the "post" template for blog posts.
* The base theme has Google Analytics built-in. If you want to use it, add <code>$config["google-analytics"]="property_id";</code> to the config file.
* There is a sample of a multi-column layout in the <code>columns.twig</code> page template - using basic bootstrap to do a classic "content on the left, list of posts on the right" style page.
* The theme is a very basic implementation of Bootstrap, which should serve as a good starting point for further development. It also makes use of the inheritance features of the Twig templating system built into Pico - so all pages are based on the "base" template, which is then appended to by "page", "post", "blog", and so on.
* At the time of release to GitHub, the theme had been tested on Pico v.1.0, and Bootstrap v.3.3.6. jQuery 1.12.3 is bundled.
