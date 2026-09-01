Prerequisites

Set up your GoGEN weather station and connect it to the internet using the Ecowitt platform - follow the user documentation that came with your station.

Access your station settings - the simplest option is to use the Ecowitt mobile application.

Important: GoGEN weather stations currently work with Windy using wu.windy.com only. The stations.windy.com endpoint does not work with GoGEN/Ecowitt stations because of their upload configuration limitations.

Initial Setup

GoGEN stations require a shorter station password. Prepare a 32-character password before configuring the Ecowitt application.



Password



Open your station's detail page in Windy Stations:My Stations -> station -> Connection.

Next to Station password, click change.

In the Rotate station password dialog, set Password length to 32 characters.

Check both confirmation checkboxes, then click Rotate password.



You will use this 32-character password as the Station Key in the Ecowitt application.

Steps

The exact configuration options may vary depending on your station model, firmware version, or the Ecowitt application version.



Settings



Open the Ecowitt application and select your weather station.

Navigate to Device Settings -> Other -> DIY Upload Servers.

Select Customized.

Set Customized to Enable.

Fill in the following fields:

Protocol Type Same As: Wunderground

Server IP / Hostname: wu.windy.com

Path: /wu? (include the final ? exactly as shown), or use wu? (without / )

Station ID: enter the Station ID of your station

Station Key: enter the 32-character Station Password you prepared above

Port: 80 for HTTP, or 443 if your station supports HTTPS

Upload Interval: 300 means 5 minutes. Do not send data more often than once every 5 minutes; otherwise, your requests will be blocked by the rate limiter. You can use a longer interval if needed.

Save your changes by clicking the Save button.

After saving, your GoGEN weather station should start sending data automatically. The first update may take a while - in some cases, up to an hour before the station becomes active and starts showing live measurements on Windy.