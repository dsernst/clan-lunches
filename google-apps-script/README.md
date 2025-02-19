This code is run in [Google Apps Script](https://developers.google.com/apps-script/?hl=en).


/* 

CLAN LUNCHES
============

## Tasks for each additional user.

1. Run "BONUS > Generate Unique Key", it will automatically create unique user keys for any rows that are missing it.
These keys are used to link responses to users. you could think of it like an API key.

2. [Optional] There's a hidden column after "What's your email?" that checks if an email address is a duplicate, and conditional formatting on the email column to highlight these dupes in red.
You probably need to extend the hidden column and conditional formatting down to apply this to new rows.

3. Generating Lat-Longs: Highlight the "What's your office address?", "Lat", and "Lng" columns in rows that missing Lat/Long values, then run "BONUS > Geocode Selected Cells".
This will look up the addresses in Google Maps API. These lat-longs are needed to calculate distances apart, used for pairing.
You can run this function multiple times over a row triplet, but it's a little slow, so only need to do it for new rows or if an address is changed.
   [Optional] There's a conditional formatter for the Lng field to highlight any entries far away from SF. This makes it easier to see any issues in the "Address" field.

4. Populate EditURL field: Run "BONUS > Get Edit URLs" function to automatically fill in the missing edit URLs. This lets users update their address and other info.
You probably want to set "Text Wrapping" to "Clip" (in the toolbar) to hide all the visual noise from these.



## Tasks to set up lunches

1. Prep all the recipients (see above: "Tasks for each additional user").

2. Send the WhatDaysAvailable? email. Make sure to give them a deadline. You probably need to edit the text of the email.

 - [ ] Update 'wkNum' in spreadsheet.gs
 - [ ] Update 'formId' in mailman.gs

3. After the deadline, run the pairing algorithm, which fills in "Wk# pair" column.

4. Send the YourMatch email to all the pairs.

5. Send the "NA" email to people who couldn't be matched

5. Celebrate.

*/

