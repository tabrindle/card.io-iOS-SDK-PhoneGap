card.io iOS plug-in for PhoneGap
---------------------------------

This plug-in exposes card.io credit card scanning.


Integration instructions
------------------------

* Add the card.io library:
    * Sign up for an account at https://www.card.io/, create an app, and take note of your `app_token`.
    * Create your cordova project
    * Add this plugin using `cordova plugin add https://github.com/tabrindle/card.io-iOS-SDK-PhoneGap`

    * Sample `canScan` usage:

      ```javascript
      window.plugins.card_io.canScan(function(canScan) {console.log("card.io can scan: " + canScan);});
      ```

    * Sample `scan` usage:

      ```javascript
      window.plugins.card_io.scan("YOUR_APP_TOKEN", {}, function(response) {
        console.log("card number: " + response["card_number"]);
        }, function() {
          console.log("card scan cancelled");
      });
      ```

License
-------
* This plugin is released under the MIT license: http://www.opensource.org/licenses/MIT
