# jquery-notific8

Notific8 is a notification plug-in inspired by the notifications introduced in Windows 8 with some web ready restyling and customizations. Notific8 has built in themes and is easy to create new themes for. The plug-in was born from a want for a simply designed yet modern and stylish notification system. The plug-in is also designed to scale based on the page's font-size setting (it was designed for the default of 100%/16px as the default).

## Demo page

An interactive demo page can be found here http://willsteinmetz.net/jquery/notific8

## Features

* Notifications slide in and out from the upper right corner of the page
* Configurable life span of the notification
* Option to display a heading
* Theme options (see CSS for built in themes)
* Ability to make the notification sticky
* Ability to set up custom settings for reuse without having to type them over and over

## Usage

    // basic
    $.notific8('My notification message goes here.');
    // with a life set
    $.notific8('My notification message has a life span.', {life: 5000});
    // with a heading
    $.notific8('My notification has a heading line.', {heading: 'Notification Heading'});
    // with a theme
    $.notific8('My notification has a theme.', {theme: 'amethyst'});
    // make the notification sticky
    $.notific8('My notification is sticky.', {sticky: true});
    // all options set
    $.notific8('My notification with all options.', {
      life: 5000,
      heading: 'Notification Heading',
      theme: 'amethyst',
      sticky: true
    });
    
    // set up your own default settings to save time and typing later
    // NOTE this is not required
    $.notific8('configure', {
      life: 5000,
      theme: 'ruby',
      sticky: true
    });


## Options

* life: number of milliseconds that the notification will be visible (default: 10000)
* heading: short heading for the notification
* theme: string for the theme (default: 'teal')
    * Custom themes should be named .jquery-notific8-notification.[theme name] in your stylesheet
* sticky: boolean for whether or not the notification should stick
    * If sticky is set to true, life will be ignored if it is also set

All of these settings are available to be configured. The configure function is used if you have specific settings such as theme and life that you want every notification to share. By configuring these settings, they become the new defaults and you don't have to type them for every notification. The configure function can be called multiple times.

## Browser support

Currently supported and testing:
* Chrome
* Firefox
* Safari (Mac only)
* IE 9+

Future support and testing
* Opera (will start after their transition to webkit)

### Browser version support

As a rule of thumb, only the most recent plus one version older of a browser is supported unless marked otherwise. While it may work in IE8, notific8 will not be tested or officially supported in legacy browsers such as versions of IE older than 9.

## Future plans

* Ability to set which edge of the screen the notifications slide in from
* Ability to set an icon for the notification
