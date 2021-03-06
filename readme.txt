=== Bulk Create Blogs ===
Contributors: gregsurname
Tags: wpmu
Requires at least: 2.8.0
Tested up to: 2.9.2
Stable tag: 2.0

A WPMU plugin for allowing the site admin to bulk create blogs using CSV data.

== Description ==

This WPMU plugin creates under the Site Admin menu called "Bulk Create Blogs" where you can bulk create/add users to blogs.

To use the plugin you must create correctly formatted data. The plugin takes
CSV formatted data where each row contains the following data.

	domain, user_id, blog_title, blog_topic,
	
Each of these fields is described below.

* blog_domain (Mandatory): the domain name of the blog, this should only contain alphanumeric characters and be in all lowercase. If the blog domain is empty then users will be added to the site's root blog.
* user_name (Mandatory): the login id of the user to be added to the blog.
* blog_title (Optional): the title of the blog.
* blog_topic (Optional): the name of the blog topic that this blog will be categorised under. These topics are setup under the 'Blog Topic Management' tab. A blog_title must be chosen if you wish to set the blog topic. (Requires cets_blog_topics plugin.) 

When each line is processed, if the blog named already exists then the user given
is added to the blog. If the blog does not exist then it is created. If a blog title
is not provided then the blog domain is used.

This plugin also provides support for LDAP user creation. If a user does not exist and 
the ldap_auth plugin is installed then it will attempt to create a new user.

At the moment this plugin only supports sites that use domain blog naming. Support for
sub-directories is not planned but you could easily add it yourself.

The number of blogs that can be imported at a time is limited.

== Installation ==

1. Upload `gb-bulk-create-blogs.php` to the `/wp-content/mu-plugins/` directory

== Frequently Asked Questions ==

== Screenshots ==

== Changelog ==

