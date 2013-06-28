# TinyTinyRSS Fever API plugin

## Description

This plugin is an open source module for TinyTinyRSS which simulates the Fever API for reading the RSS Feeds with your Fever clients.

- - -

* <a href="#features">Features</a>
* <a href="#download">Downloads</a>
* <a href="#supported">Supported/Tested Clients</a>
* <a href="#installation">Installation</a>
* <a href="#debug">Debugging</a>
* <a href="#license">License</a>
* <a href="#changelog">Changelog</a>

## <a name="features">Features</a>

Following Features are implemented:

* getting new RSS items
* getting starred RSS items
* setting read marker for item(s)
* setting starred marker for item(s)
* hot is **not** supported

## <a name="downloads">Downloads</a>

Please click the ```ZIP``` Button to download current version. ;)

## <a name="supported">Supported/Tested Clients</a>

These clients should be working fine with this API emulation.

* Reeder - iPhone
* Mr.Reader - iPad

## <a name="installation">Installation</a>

Upload the ```fever``` folder in the ```plugins``` folder of your TinyTinyRSS installation. Enable the plugin in the preferences and set your password for the Fever API.

See [here](http://tt-rss.org/forum/viewtopic.php?f=22&t=1981) for more detailed informations.

## <a name="debug">Debugging</a>

In the file ```fever_api.php``` there are two flags for debugging at the beginning of the file.

* ```DEBUG``` - set this to true to get a fever_debug.txt file in your root folder of the Tiny Tiny RSS installation.
* ```DEBUG_USER``` - set this to the id (from ttrss_users) of your user you would like to always authenticate on your Tiny Tiny RSS installation. The authentication process is then skipped and the api gets always authentication.
* ```DEBUG_FILE``` - set this to a filename that suits you for debugging this plugin if you need to.

## <a name="license">License</a>

Licensed under GNU GPL version 2 (<- I think this is okay for this plugin…)

## <a name="changelog">Changelog</a>

v1.0-v1.2 - 2013/5/27 - DigitalDJ version

* see this [thread](http://tt-rss.org/forum/viewtopic.php?f=22&t=1981) in the TinyTinyRSS Forum

v1.3 - 2013/6/27

* fixed several bugs in json output from the plugin
* added a small fix for Mr.Reader 2.0 so it can complete loading of all items (see [FAQ](http://www.curioustimes.de/mrreader/faq/))
* added first Mr.Reader compatiblity without marking items read/starred
* changed the field ```date_entered``` to ```updated``` for better reading experience

v1.4 - 2013/6/28

* fixed authentication with Mr.Reader 2.0
* fixed debugging options

v1.4.1 - 2013/6/28

* removed password from debug log file

v1.4.2 - 2013/6/28

* changed the ```DEBUG_USER``` evaluation a little bit for disabling authentication without DEBUG = true

v1.4.3 - 2013/6/28

* added ```DEBUG_FILE``` to debug configuration
* changed authentication call from Mr.Reader so that the reply is also uppercase, since the API-KEY comes in uppercase from clients
* fixed debug output while authentication in Mr.Reader with displaying the email adress