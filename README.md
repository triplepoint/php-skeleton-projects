# Introduction
Every time I start a new PHP project, I end up spending 20 minutes organizing the directories and obsessively tweaking the config files.  I'm tired of doing that, so here's my templates.  From here on out, it's goodbye OCD project anxiety, and hello copy/paste/find/replace simplicity.

# Usage
## Copy/Paste and Git
Copy the appropriate project type into a new directory, initalize it as a git project, and make the first commit.  For example:

``` bash
cd {some working directory}
cp -R php-skeleton-projects/composer-library some-new-project
cd some-new-project
find . -name "delete_me.del" -type f -delete
git init
git commit -a -m "Initial commit - cloned from triplepoint/php-skeleton-projects."
```

## Customize
### Project Names
Find/Replace `PROJECT_NAMESPACE` with a PHP namespace like `MyNewProject`.  Be sure to rename the `/source/PROJECT_NAMESPACE` subdirectory and the `/test/PROJECT_NAMESPACETest` subdirectory.

Find/Replace `PROJECT_TITLE` with an appropriate git project name - something all lower case and with dashes instead of underscores, like `my-new-project`.

Find/Replace `{CURRENT_YEAR}` with the current year.

### If You're Not Jonathan Hanson
If you're not me, please Find/Replace `triplepoint/` (case-sensitive) with your own GitHub username.  Also, please search for `jonathan` (case-insensitive) and revise the identities appropriately.

### Prune Any Unwanted Directories
I have a few common directories in place here (especially for the projects) like `cache` and `configuration`, etc.  Prune out any you don't need.

### Commit
``` bash
git commit -a -m "Customizes project skeleton."
```

## Travis-CI
If this is a public repository, you should consider registering it with Travis-CI, and setting up the GitHub callback.

## Packagist.org
If this is a public library, you should consider registering it with Packagist.org, and setting up the GitHub callback.

## Done
At this point, you should have a reasonably useful skeleton in which to start development.  First step is probably to start adding Composer dependencies to the `composer.json` file (see [Packagist.org](https://packagist.org/)), and then do a `composer install`.

OCD Vanquished.  Good luck.
