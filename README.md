# Introduction
Every time I start a new PHP project, I end up spending 20 minutes organizing the directories and obsessively tweaking the config files.  I'm tired of doing that, so here's my templates.  From here on out, it's goodbye OCD project anxiety, and hello copy/paste/find/replace simplicity.

# Usage
## Copy/Paste and Git
Copy the appropriate project type into a new directory, initalize it as a git project, and make the first commit.  For example:

``` bash
cp thisdir/composer-library ../new_project_directory
git init
git commit -a -m "Initial commit."
```

## Customize
### Project Names
Find/Replace `PROJECTNAME` with an approprite git project name - something all lower case and with dashes instead of underscores, like `my-new-project`.

Find/Replace `PROJECTNAMESPACE` with a PHP namespace like `MyNewProject`.  Be sure to rename the `/source/PROJECTNAMESPACE` subdirectory and the `/test/PROJECTNAMESPACETest` subdirectory.

### If You're Not Jonathan Hanson
If you're not me, please Find/Replace `triplepoint/` (case-sensitive) with your own GitHub username.  Also, please search for `jonathan` (case-insensitive) and revise the identities appropriately.

## Prune Any Unwanted Directories
I have a few common directories in place here (especially for the projects) like `cache` and `configuration`, etc.  Prune out any you don't need.

### Commit
``` bash
git commit -a -m "Customizes project skeleton."
```

## Done
At this point, you should have a reasonably useful skeleton in which to start development.  First step is probably to start adding Composer dependencies to the `composer.json` file (see [Packagist.org](https://packagist.org/)), and then do a `composer install`.

OCD Vanquished.  Good luck.
