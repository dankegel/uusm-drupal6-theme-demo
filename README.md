This is a simple demo of the uusm theme, using a drush profile to
(at least theoretically) make installing easier.
(Later, we'll use the same mechanism to create a working demo of the
entire uusm site, not just its theme.)

To try it out:

1) Do the usual prerequisites, e.g. install apache, mysql, drush, etc.
and set up a fresh database. (If you're on Ubuntu, see e.g. the first part of
https://www.digitalocean.com/community/articles/how-to-install-drush-on-a-cloud-server-running-ubuntu-12-04 )

2) Do

    git clone https://github.com/dankegel/uusm-drupal6-theme-demo.git
    cd uusm-drupal6-theme-demo
    drush make uusm-theme-demo.make

3) Copy sites/default/default-settings.php to sites/default/settings.php
and edit to point to your database

4) Create the directory sites/default/files and mark it writable
so so the uusm theme can write to it
(e.g. mkdir -p sites/default/files; chmod 777 you-know-what.  This is dangerous.)

5) Set up your web server to make uusm-drupal6-theme-demo the document root,
and turn on AllowOverride as usual to allow clean URLs.

6) Open the site in a browser (e.g. http://localhost );
you should see the normal Drupal 6 installation page, but with a
uusm-theme-demo profile.  Choose that!
(You might need to visit http://localhost/install.php explicitly if you
put database info into settings.php already.)

7) Using the usual admin web interface, enable the UUSM theme and make it the
default.  (Hmm, why didn't the profile do that?)

8) Go to the site's home page.  Notice all the 'Undefined index' warnings.  What's up with that, eh?
