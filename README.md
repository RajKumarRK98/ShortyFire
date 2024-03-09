# ShortyFire
## Requirements:
 1. Local DB with Schema
 2. Service side handling to save data
 3. User interaction
	 1. save incoming IP in DB for every link visit if it does not exist already.
 4. Shortening Business logic
	 1. Generate unique characters for input link
	 2. Map the generated link to input in DB
	 3. Generate QR for generated link with unique parameter to say it is from QR or link.
 5. Redirect Business logic
	 1. Upon visiting shortened link check if it exists in DB
	 2. If exists proceed to redirect else return to homepage saying "Expired or Invalid"
	 3. Upon using QR and visiting shortened link repeat 1 and 2 as necessary
6. Tracking Logic
	1. Track QR visits using the unique query param embedded in link, if param track as QR else direct link
	2.  Check if incoming IP is present in DB and track as unique if it is not there.
	3. Count the total visit if it is there.
7. Schema Details
	1. have activate / deactivate flag with generated link and user details. 

##

## Optional

 1. Have a cron job to auto deactivate the URLs generated by guest users after 24 hours.
 2. Have a feature to let users configure their custom domain and generate links under them.
 3. Generate SSL certificates for the custom domains.
