# Twitch Chat Messages as DVD Logos

Boost chat activity and retain viewers during Starting-Soon and BRB screens with this little game. Chat messages from your Twitch channel bounce around and take damage.


![DVD Demo](dvd-demo.gif)



## Features
- Twitch chat messages become bouncing boxes  
- Messages can collide and take damage  
- Additional messages from the same chatter heal their box
- Customizable settings  
- Optional countdown in the background
- Use your own background image / scene


## How to Use in OBS
This is a lightweight, all-in-one HTML file.

1. Download `dvd-fight.html`.
2. Open OBS.
3. Add a **Browser Source**.
4. Click the checkbox "Local File"
4. Browse and select the file where you saved it (The path should then be something like`file:///C:/Users/YourName/Downloads/dvd-fight.html`)
5. Set the size to your streaming resolution (should work with any, tested with 1920x1080).
6. Click the checkbox "Shutdown source when not visible" or "Refresh browser when scene becomes active" (This will restart the countdown when you change scenes)

You can test that is works by typing a message in your offline chat.

**NOTE:** The game background is transparent; so whatever you put behind it in OBS will peek through (e.g., your usual starting-soon art)


## Editing Settings

Before using this in OBS you must edit the settings (at the very least set your channel name).

At the top of the `.html` file, you'll find a section that looks like this:

```js
// --- --- --- --- --- --- --- --- SETTINGS --- --- --- --- --- --- --- ---
// ONLY EDIT THE LEFT SIDE OF THE EQUATION

// replace "nikosiaphd" with your twitch channel name
const CHANNEL_NAME = "nikosiaphd"

// messages from these accounts won't spawn boxes
const EXCLUDED_CHATTERS = ["soundalerts"]

// Adjust how big the boxes are. 1.0 is default, 1.5 is 50% bigger, etc.
const BOX_SCALE = 1.5

// "true" if you want to show the countdown timer, "false" if you don't
const SHOW_TIMER = true 

// How long should the countdown timer be? (in minutes)
const TIMER_MINUTES = 11

// Show hours (the first 00: to the left) in the countdown timer
const SHOW_HOURS = true

// Show milliseconds (the fast .00 to the right) in the countdown timer
const SHOW_MILLISECONDS = true

// "true" if you want the timer to flash every couple of seconds, "false" if you don't
const TIMER_FLASHING = true

// AFTER THIS LINE YOU SHOULD NOT EDIT ANYTHING UNLESS YOU KNOW WHAT YOU'RE DOING
// --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- --- ---
```

Edit these values as needed. Save the file and reload it in OBS ("Refresh Cache") to apply changes.


## Contact, Future Plans, etc.

You are free to use and modify this for your own stream. Instead of sharing the code with anyone ("redistribution"), refer them to this github repository. 

Feel free to contact me with suggestions or questions.

Features I want to add at some point:
- kill feed in one of the corners
- scoreboard in one of the corners

