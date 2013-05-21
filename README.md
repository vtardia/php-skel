PHP Skel
========

A PHP Skeleton Project template buildable with [Phing](http://www.phing.info)


## Installation

You can create a new skeleton project using `composer.phar`:

    $ php composer.phar create-project vtardia/php-skel your-project-directory    

or simply download [php-skel.zip](https://github.com/vtardia/php-skel-package/blob/master/php-skel.zip?raw=true), extract it where you want and rename it.


## Requirements

In order to deploy skeleton projects you will need:

 - [Phing](https://github.com/phingofficial/phing)
 - [FileSyncTask Extension](https://github.com/fedecarg/phing-filesynctask)
 
These dependencies are not included in the `composer.json` for this package because you may want to install them globally on your machine (ex. inside `/usr/share/php/phing`).

If you need them as project's requirements insert these lines in your  `composer.json` file:

    "require": {
        "phing/phing": "*"
    },

    "scripts": {
        "post-install-cmd": [
            "wget https://raw.github.com/fedecarg/phing-filesynctask/master/tasks/ext/FileSyncTask.php -O ./vendor/phing/phing/classes/phing/tasks/ext/FileSyncTask.php"
        ]
    },

**Note**: the `scripts` section is necessary because the `FileSyncTask` provided with Phing is not in sync.


## Sample Skeletons

The following sample installs a basic web app with [Slim Framework](http://slimframework.com), [Monolog](https://github.com/Seldaek/monolog), [Paris & Idiorm](http://j4mie.github.io/idiormandparis/) and [Swiftmailer](http://swiftmailer.org).

    "require": {
        "php": ">=5.3",
        "ext-zip": "*",
        "ext-fileinfo": "*",
        "slim/slim": "*",
        "slim/extras": "*",
        "monolog/monolog": "*",
        "j4mie/paris": "*",
        "swiftmailer/swiftmailer": "*"
    },


## References

 - [Using Phing, the PHP Build Tool](http://phpmaster.com/using-phing/) by [Shameer C](http://shameerc.com/)
 - [Deploy and Release your Applications with Phing](http://phpmaster.com/deploy-and-release-your-applications-with-phing/) by [Vito Tardia](http://vtardia.com)


## License

**PHP Skel** is licensed under the MIT license.
