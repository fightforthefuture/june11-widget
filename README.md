# June 11, 2018 Widget

This is the source code for Battle for the Net's June 11 day of action widget. Net neutrality ends June 11th, but the fight has just begun. [Click here to learn more.](https://www.battleforthenet.com/)

## How to install the widget on your site

Add this one line of JavaScript to any page, and you're good to go: ([**See the demo!**](https://www.fightforthefuture.org?widget=june11))

```html
<script src="https://june11.battleforthenet.com/widget.js" async></script>
```

You can change the positioning and do some customization via the `BFTN_WIDGET_OPTIONS` [described below](#customization-options).

If you have any problems or questions regarding the widget, please [submit an issue](https://github.com/fightforthefuture/june11-widget/issues).


## How it works

Add this widget to your site to display the following message at the bottom right (or left) side of the screen:

![A screenshot of the minimized widget](https://www.battleforthenet.com/images/june11-widget-screenshot.jpg)

Clicking the message will open up this form, allowing visitors to send a letter to congress without leaving your site:

![A screenshot of the minimized widget](https://www.battleforthenet.com/images/june11-widget-maximized.jpg?v=2)

The widget is designed to appear once per user, per device, per day, but can be configured to display at a different interval. If you'd like to force it to show up on your page for testing, reload the page with `#ALWAYS_SHOW_WIDGET` at the end of the URL.

Please take a look at [**widget.js**](https://github.com/fightforthefuture/june11-widget/blob/master/static/widget.js) if you want to see exactly what you're embedding on your page.

The widget is compatible with Firefox, Chrome (desktop and mobile), Safari (desktop and mobile), Microsoft Edge, and Internet Explorer 11.

## Customization options

If you define an object called `BFTN_WIDGET_OPTIONS` before including the widget code, you can pass some properties in to customize the default behavior.

```html
<script type="text/javascript">
  var BFTN_WIDGET_OPTIONS = {
    /**
     * Sets the position of the widget on the page. Can be 'left' or 'right'.
     * Defaults to 'right'.
     */
    position: 'right', // @type {string}

    /**
     * Set the language of the widget. Can be "en" for English or "es" for Spanish.
     * Defaults to null, which will obey the nagivator.language setting of the 
     * viewer's browser.
     */
    language: null, // @type {string}

    /*
     * Choose from 'fp' for Free Press, 'dp' for Demand Progress or
     * 'fftf' for Fight for the Future. Omit this property to randomly split
     * form submissions between all organizations in the Battle for the Net 
     * coalition. Defaults to null.
     */
    org: null, // @type {string}

    /*
     * Specify view cookie expiration. After initial view, modal will not be
     * displayed to a user again until after this cookie expires. Defaults to 
     * one day.
     */
    cookieExpirationDays: 1, // @type {number}

    /*
     * Prevents the widget iframe from loading Google Analytics. Defaults to 
     * false. (Google Analytics will also be disabled if doNotTrack is set on
     * the user's browser.)
     */
    disableGoogleAnalytics: false, // @type {boolean}

    /*
     * Prevent the donate button from showing. Defaults to false.
     */
    disableDonations: false, // @type {boolean}
    
    /*
     * Always show the widget. Useful for testing. Defaults to false.
     */
    alwaysShow: false, // @type {boolean}

    /*
     * Automatically maximizes the widget. Defaults to false.
     */
    alwaysMaximize: false // @type {boolean}
  };
</script>
<script src="https://june11.battleforthenet.com/widget.js" async></script>
```
