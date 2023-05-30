# MZagmajster Iso Code Bundle

This plugin adds iso coutrny code (ISO2) to a contact based on what Mautic country is selected from the dropdown.

## Getting Started

### Prerequisites

* Composer 1
* Mautic 4


### Installing

Use hooks from .githooks folder on project by executing:

```
./bin/init.sh
```

**Initial install** described below.

```
cd <mautic-root-folder>
rm -rf var/cache/dev/* var/cache/prod/*
cd plugins
git clone <repo-url> MZagmajsterIsoCodeBundle
cd <mautic-root-folder>
composer install  # You only need this druing development.
php bin/console mautic:plugins:install --dev  # You should get a message saying one or more plugins have been installed in terminal.
```


Typical **update** of plugin source code described below.

* Make sure plugin root folder is clean from git´s point of view.

```
cd <mautic-root-folder>
rm -rf var/cache/dev/* var/cache/prod/*
cd plugins/MZagmajsterIsoCodeBundle
git pull origin <branch>
php bin/console mautic:plugins:reload --dev  # You should get a message saying one or more plugins have been installed in terminal.
```

## Running the tests

[No tests yet.]

### Coding style

Please refer to PHP CS file for details on coding styles.

From plugin root folder you can also run the following commands during development.

* ```composer lint``` - Checks the PHP syntax.
* ```composer checkcs``` - Checks code formatting && show what should be fixed (does not touch source files).
* ```composer fixcs``` - Fixes code formatting (updates soruce files).

## Deployment

* You do not have to install any composer packages inside plugin folder since we only use it during development.
* When you are deploying the plugin make sure you call ```php bin/console``` command without --dev switch.

## Changelog

[No changelog yet.]

## Documentation

* Inside CustomContactFields.php you set the alias for iso country code field you are gonna use to store the value.
* Clear the cache and reload the plugin.
* Create custom field as you specified in the plugin file.
* Test it: create a contact and then select the country from the mautic dropdown, when you save, there should be ISO country code present in the custom field you created.

## Built With

* [Mautic](https://github.com/mautic/) - Open Source Marketing Automation Tool
* [Composer](https://getcomposer.org/) - Dependency Management

## Contributing

- If you have a suggestion for the feature or improvement consider opening an issue on GitHub (just make sure the same issue does not already exists).
- If you want, you can open a pull request and I will make an effort to merge it.
- Finally if this project was helpful to you consider supporting it with a donation via [PayPal](https://paypal.me/maticzagmajster). Thank you!

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the tags on this repository. 

## Authors

Content in this project was provided by [Matic Zagmajster](http://maticzagmajster.ddns.net/). For more information please see ```AUTHORS``` file.

## Acknowledgments

* Thanks to entire Mautic Community for providing awesome marketing automation tool.



