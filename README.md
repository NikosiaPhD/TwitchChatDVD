# Twitch Chat Messages as DVD Logos

Boost chat activity and retain viewers during Starting-Soon and Be-Right-Back screens with this little game. Chat messages from your Twitch channel bounce around and take damage.


![DVD Demo](dvd-demo.gif)



## Features
- Twitch chat messages become bouncing boxes  
- Messages can collide and take damage  
- Additional messages from the same chatter heal their box
- Customizable settings  
- Optional kill feed and scoreboard
- Transparent background so you can use your own background image / scene


**NOTE:** 

- The game background is transparent; so whatever you put behind it in OBS will peek through (e.g., your usual starting-soon art)
- The timer that you see in the demo above is no longer included in this. I might provide it as a separate download at some point.
- The font file is not included. So, the text will look a little bit different for you.


## How to Use in OBS
This is a lightweight, all-in-one HTML file.

1. Download `dvd-fight.html`.
2. Open OBS.
3. Add a **Browser Source**.
4. Click the checkbox "Local File"
4. Browse and select the file where you saved it (The path should then be something like`file:///C:/Users/YourName/Downloads/dvd-fight.html`)
5. Set the size to your streaming resolution (should work with any, tested with 1920x1080).

You can test that is works by typing a message in your offline chat.




## Editing Settings

Before using this in OBS you must edit the settings (at the very least set your channel name).

At the top of the `.html` file, you'll find a section that looks like this:

```js
// --- --- --- --- --- --- --- --- SETTINGS --- --- --- --- --- --- --- ---
// ONLY EDIT THE LEFT SIDE OF THE EQUATION

// replace "nikosiaphd" with your twitch channel name
const CHANNEL_NAME = "nikosiaphd"

// messages from these accounts won't spawn boxes
const EXCLUDED_CHATTERS = ["soundalerts", "streamelements", "sery_bot", "nightbot"]

// Adjust how big the boxes are. If 1.0 is a bit small, 1.5 makes it 50% bigger, etc.
const SCALE = 1.5

// change "true" to "false" if you don't want the kill feed or the highscore list to show up
const SHOW_KILL_FEED = true
const SHOW_HIGHSCORE_LIST = true

// AFTER THIS LINE YOU SHOULD NOT EDIT ANYTHING UNLESS YOU KNOW WHAT YOU'RE DOING
// --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- ---
```

Edit these values as needed. Save the file and reload it in OBS ("Refresh Cache") to apply changes.


## Contact, Future Plans, etc.

You are free to use and modify this for your own stream. Instead of sharing the code with anyone ("redistribution"), please refer them to this github repository. 

Don't hesitate to contact me with suggestions or questions.

