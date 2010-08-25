## CakeSocial CakePHP Plugin ##

The CakeSocial plugin for CakePHP allows for simple integration of social media into your CakePHP application.

## CakePHP Version ##

This plugin is built for CakePHP 1.3 and above.

Upgrade from CakePHP 1.2 to CakePHP 1.3 takes about 5 minutes, checkout the awesome [migration guide](http://book.cakephp.org/view/1561/Migrating-from-CakePHP-1-2-to-1-3).

## Installation ##

### Downloading an archive ###

If you downloaded a tar.gz, tar.bz2 or zip file, extract the contents of the archive to your applications `/plugins` directory.

The result will be a `cake_social` directory under your `plugins` directory.

### Using a git submodule ###

Navigate to the root of your application, and add the CakeSocial plugin as a submodule with the following git command:

	git submodule add plugins/cake_social http://github.com/predominant/cake_social.git
	git submodule init
	git submodule update

## Usage ##

The simplest method of usage is to include each helper you want to use on your AppController class.

If you do not have one already, create the file `app_controller.php` in the root of your application, and add the following:

	<?php
	App::import('Helper', 'CakeSocial.ShareThis');

	class AppController extends Controller {
		public $helpers = array(
			'CakeSocial.ShareThis' => array(
				'publisher' => 'my-publisher-id',
			),
			'Session'
		);
	}

Now you can just display the widget on any page with the following CakePHP view code:

	echo $this->ShareThis->display();

Simple!

## Comments, Suggestions, and other... ##

I'd be more than thrilled to hear anyones experiences with this CakeSocial plugin.

If you have suggestions, enhancement requests, or bugs, please let me know.
