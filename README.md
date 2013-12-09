This is a simple demo of the uusm theme, using a drush profile to
(at least theoretically) make installing easier.
(Later, we'll use the same mechanism to create a working demo of the
entire uusm site, not just its theme.)

To try it out:

1) set up a fresh database

2) Do

    git clone https://github.com/dankegel/uusm-drupal6-theme-demo.git
    cd uusm-drupal6-theme-demo
    drush make uusm-theme-demo.make

3) Copy sites/default/default-settings.php to sites/default/settings.php
and edit to point to your database

4) Fix permissions on sites/default/files so the uusm theme can write to it
(e.g. chmod 777 you-know-what.  This is dangerous.)

5) Open the site in a browser (e.g. http://localhost );
you should see the normal Drupal 6 installation page, but with a
uusm-theme-demo profile.  Choose that!

6) Notice all the 'Undefined index' warnings.  What's up with that, eh?
