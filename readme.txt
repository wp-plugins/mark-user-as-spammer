=== Mark User as Spammer ===
Contributors: korobochkin
Donate link: https://www.paypal.com/cgi-bin/webscr?cmd=_donations&business=me%40korobochkin%2ecom&lc=EN&item_name=For%20plugin%20Mark%20user%20as%20spammer&currency_code=USD&bn=PP%2dDonationsBF%3abtn_donate_SM%2egif%3aNonHosted
Tags: spammers, ban, block users, spam, accounts, login, blacklist
Requires at least: 4.1.1
Tested up to: 4.2.1
Stable tag: 1.0.2
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

The ability to mark specific users as spammers like on Multisite install.

== Description ==

The ability to mark specific users as spammers like on Multisite install. If you mark user as spammer he can't log in into WordPress and got an error shows up that account have been marked as spammer account. This behavior grabbed from WordPress Multisite install.

Helpfull if you want disable login for some user but don't want to delete account. Deleting account is not good idea because you can delete good account. Or delete spammer account but it can be mistake. After deleting you can't restore account but with this plugin you can ban or unban accounts anytime.

You can ban or unban users on /wp-admin/users.php page by clicking links bellow username. Be careful, you can ban yourself, administrators or other highlevel users.

You can also switch account status by manually editing `mark_user_as_spammer` user meta in `wp_usermeta` table. `1` — spammer. `0` — not spammer.

[Plugin on Github](https://github.com/korobochkin/mark-user-as-spammer)

Photo on banner created by [Bastian Sara](https://stocksnap.io/photo/LVKUG7VU8F).

== Installation ==

= From your WordPress dashboard =

1. Visit 'Plugins > Add New'
2. Search for 'mark user as spammer'
3. Activate Mark User as Spammer from your Plugins page.
4. Ban or unban users on yourdomain.com/wp-admin/users.php page.

= From WordPress.org =

1. Download Mark User as Spammer.
2. Upload the 'mark-user-as-spammer' directory to your '/wp-content/plugins/' directory, using your favorite method (ftp, sftp, scp, etc...).
3. Activate Mark User as Spammer from your Plugins page.
4. Ban or unban users on yourdomain.com/wp-admin/users.php page.

== Screenshots ==

1. Ban or unban users on Users page. Blocked users marked with red background.
2. If you ban someone he can't log in anymore and WordPress shows up the error notice during login process.

== Frequently Asked Questions ==

= Which information plugin stores in DB? =

The plugin add only single user meta option to each user with meta_key equal 'mark_user_as_spammer'. On uninstall action plugin completely remove this metas for all users.

== Changelog ==

= 1.0.2 =
* Prepare URL before output it. This plugin doesn't have XSS vulnerability like many others plugins (because we use `wp_nonce_url()` before output the links) but page may look incorrect if you try to open something like `site.com/users.php?"><script>alert('hi')</script>`. Script not working (thanks `wp_nonce_url()`) but markup looks crashed.

= 1.0.1 =
* Translated all comments in code to english.
* Added plugin icon, banner and screenshots.
* Fixed WordPress required and tested up versions.
* Improved readme file.

= 1.0.0 =
* First version of plugin.

== Upgrade Notice ==

= 1.0.2 =
Security improvements release. Better output for the links.

= 1.0.1 =
Fixed WordPress required and tested up versions.
