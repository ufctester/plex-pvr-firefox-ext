plex-pvr-firefox-ext
==============

Features
------------------------------------------------------------------------
- Adds link to view the trailer for movies within Plex/Web

Contributors
------------------------------------------------------------------------
* [ufctester](https://github.com/ufctester)

Version History
------------------------------------------------------------------------
- **v0.0.1** - Initial checkin

Building the extension
------------------------------------------------------------------------
There are 2 ways to build.  
To build using jpm you need to install jpm
     
    npm install jpm --global
        jpm init	Create a skeleton add-on as a starting point for your add-on.
        jpm run	Launch an instance of Firefox with your add-on installed.
        jpm test	Runs your add-on's unit tests.
        jpm xpi	Package your add-on as an XPI file, which is the install file format for Firefox add-ons.
        jpm post	Package your add-on as an XPI file, and then post it to some URL.
        jpm watchpost	Package your add-on as an XPI file whenever there is a file change and post that to some URL.
        jpm sign	Package your add-on as an XPI file, and then retrieve a new XPI signed by Mozilla.

    Packaging
        This command packages the add-on as an XPI file, which is the install file format for Mozilla add-ons.
        jpm xpi --dest-dir C:/temp

        
To build download and install the [Add-on SDK](https://developer.mozilla.org/en-US/Add-ons/SDK), cd to the extension source code directory and run:

    <sdk_directory>/bin/cfx xpi

To run it in a developers profile run:

    <sdk_directory>/bin/cfx run

Running the extension without creating an xpi for debugging
------------------------------------------------------------------------
    npm install jpm --global
        jpm init	Create a skeleton add-on as a starting point for your add-on.
        jpm run	Launch an instance of Firefox with your add-on installed.
        jpm test	Runs your add-on's unit tests.
        jpm xpi	Package your add-on as an XPI file, which is the install file format for Firefox add-ons.
        jpm post	Package your add-on as an XPI file, and then post it to some URL.
        jpm watchpost	Package your add-on as an XPI file whenever there is a file change and post that to some URL.
        jpm sign	Package your add-on as an XPI file, and then retrieve a new XPI signed by Mozilla.

        
        
    Run Add-ons
        jpm run -b "C:\Program Files (x86)\Firefox Developer Edition\firefox.exe"

    
Enabling debugging
------------------------------------------------------------------------
In the extension settings page enable debug mode. By default `console.log()` statements in SDK addons won't show up in the browser console. To allow them to show up you will need to open up `about:config`, create a new preference, name it `extensions.sdk.console.logLevel` and set the value as `all`.


