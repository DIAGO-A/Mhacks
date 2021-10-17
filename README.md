## Inspiration
I thought of using Assembly AI in some smart way and came up with the door lock system idea which can open the door lock using otp sent to registered mobile with twilio API.
I had also used google cloud vision API for number plate detecting and operating the door using the predefined number plate stored in the cloudant db.
## What it does
I basically hears a predefined command from the user and transcribe using assembly AI if the command matches it sends a 3-digit temporary OTP (valid for only 40 sec) to the registered admin's phone number.
The otp has to be given using voice command to the app, if it matches it opens the door and closes automatically after 15 sec.
 had also used google cloud vision API for number plate detecting and operating the door using the predefined number plate stored in the cloudant db.
## How we built it
Fist we transcribe the voice command using assembly AI and check in the backend with the predefined command if it exist we send a random 3 digit otp using twilio.
the otp is then again transcribed using assembly AI and if matches it reset the otp immediately.
While using the google cloud vision API the admin's car number plate is already stored in the Cloudant db, when the image is sent to the vision api it checks for the OCR and node red matches it with the cloudant db if it matches it opens the door and closes after 15 sec.

## Challenges we ran into
1. To use assembly AI to transcribe the OTP
2. TO get the desired OCR from vision API

## Accomplishments that we're proud of
I had came up with the thing that I had planed to make within this small span of time!
## What we learned
1. google vision api
2.Assembly AI
3. TWilio
4. how to change buffer into base64 encoding in node red.
