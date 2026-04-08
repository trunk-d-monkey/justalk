   This application will parse the conversations from the JusTalk app
   (tested on iOS) into an SQLite database for analysis. This was working on version 8.9.44 for iOS
   which was out around early 2026.  The app looks to be updated to work with multiple party
   threads and video.  At the time this was made, it only appeared to allow person to person
   communications.  The data also didn't seem to list any time of participants list or anything
   similar to what we see with SMS.db or other similar chat apps.  This worked fine for the case
   it was used for and you're welcome to try it.  
   
   Files and folders it needs are:
   
   Main Realm Database: 
      [app container]/data/[user id]/realm/[user id].realm
   
   Cache Folder:
      [app container]/data/imageCache/temp
   
   INSTRUCTIONS: Export the above file and folder.  Use RealmStudio to
   export the realm database AS a JSON file. You can then point the 
   input and folder arguments to process the file. 
   
   EX: python parse_justalk.py -i D:\JUSTALK_DATA\9999_62135600.json 
   -f D:\JUSTALK_DATA\data\imageCache\temp
