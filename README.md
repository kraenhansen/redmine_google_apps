Google Apps login for Redmine
=============================

This Redmine plugin allows you to login using your Google Apps domain's user.

Differences from original plugin by Juan Wajnerman
------------

* Full support Redmine 2.x
* "On the fly user creation" option
* Google App authentication mode moved to *Authentication modes* menu in an Administration zone (old LDAP Authentication menu field)

Requirements
------------

* Redmine 2.3.x or newer
* Google Apps domain (your @gmail account will not work)

Install
-------

Clone the plugin source code into your Redmine's plugin directory.

    git clone git://github.com/dmitrynop/redmine_google_apps.git plugins/google_apps

**NOTE:** Make sure the plugin directory is name `google_apps`.

Copy plugin assets to a public directory.

    rake redmine:plugins:assets

Setup
-----

Login with your administrator account, go to the Administration section and now you should see the 'Google Apps' link. Add your Google Apps domain like 'example.com'. (Note, it's not www.example.com).

Logout and go to the login page again. Now a link to login with your Google Apps domain should be visible.

Troubleshooting
---------------

**OpenID verification failed**
* check permissions on [redmine]/tmp/cache - try to set 777
