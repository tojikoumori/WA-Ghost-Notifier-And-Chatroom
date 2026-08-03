# 2000s-WhatsApp-Notifier-Chatroom

### Overview

_Message deliverers / Notifier_ :

https://github.com/user-attachments/assets/1e8728c6-6bf1-4234-853b-b0a5707955d1

<img width="1080" height="676" alt="Image" src="https://github.com/user-attachments/assets/b193b907-805c-4797-9ee6-1c4fba84867a" />

_Chat room!_ (Will be referred to as 'UI') :

(tweaked version: **publishing soon!!** needs some touch ups)
<img width="1917" height="1020" alt="Senza titolo 237_20260803190353" src="https://github.com/user-attachments/assets/1c8236ac-74a0-4776-932f-2f4f3b00f04e" />

<img width="680" height="104" alt="immagine" src="https://github.com/user-attachments/assets/f1fffe16-07c9-4789-8bb9-b5d222e2eb09" />

-----------------------------------
<sup>i make projects for fun and share them to use freely, though i spend so much time on them, 

<sup>so if this was of use to you and you want to support me i appreciate donations :)<sup>

<sup>☕ https://buymeacoffee.com/tojikoumori<sup>

-------------------------------------

### Infos / Other required downloads

_This script makes use of [Bayleys](https://github.com/whiskeysockets/Baileys) and works by using the official WhatsApp Linked Device protocol: the script functions just like a web browser. It doesn't store your personal data, and it operates entirely offline on your own computer._

_It has been designed to work and be paired with this specific [Kaomoji Ghost](https://web.archive.org/web/20070113064539/http://www.geocities.co.jp/Bookend-Shikibu/8267/nanikapnew.htm)_ 

_You can download the SSP software [here](https://ssp.shillest.net/) needed for the Kaomoji Ghost_ 


### Features 

• The ghost(s) will play their idle animation, until you receive a message.

• You will see an HOLD icon (which can be swapped for another custom one if you'd like) that'll only disappear upon having read the message. 

• Plays custom sound when a message is received

• Operates silently (no cmd popping/staying) and on your app tray

• From your tray, you can choose to hide the Ghosts/show them again, and open the log to know what's happening

• From the already built-in SSP feature, you can choose to show the Ghosts on top of every page / resize them at will 

• The UI stays on your taskbar, and has a whatsapp icon.

• It's been designed to have a 2000s-ish japanese chatroom aesthetic - although I would like to polish it

• You can import your full chat history from whatsapp to the UI

• You can send and import stickers from sticker.ly to the UI

• Full media viewing / audio listening support (you can zoom on images, too)

• You can reply to / quote specific messages directly in the UI

• You can pick a custom background wallpaper for the UI

• Your and your contact's profile picture is directly fetched from whatsapp

• Your incoming messages and the imported chat history will be cached and saved directly in your computer

• You can look up specific messages in a chat with the search feature

### Setup instructions

### 1. Installing dependencies

Step 1: Open the Terminal in the Right Place

Open the extracted wa_listener folder in Windows File Explorer.

Click on the address bar at the very top of the window (where it says C:\Users\...).

Delete everything in the bar, type cmd, and press Enter.

A black terminal window will pop up, already perfectly locked into your folder!

Step 2: The Copy-Paste Commands

Once that black window is open, just run these three commands, one at a time. 

1. Install the Node.js Background Stuff


**npm install @whiskeysockets/baileys pino systray qrcode qrcode-terminal**

2. Install the Python Visual Stuff
This downloads the tools needed to draw the user interface:

**Bash**

**pip install pywebview emoji**

If any of these commands say 'npm is not recognized' or 'pip is not recognized', it means you haven't installed Node.js or Python yet! Go download and install those first.

### 2. Configure your target numbers

In the data folder, after connecting to whatsapp scanning the qr code in the UI (launch start_silent.vbs), you will find a contacts_cache.json -- open it

use the Find option to search for your desired contact's name/s, and note the digits before @lid

In the same data folder, you will find a config.json, fill the template

### 3. Ghost Assets

Navigate to the `Ghost_Assets` folder.

Copy the provided image file (or use a custom one) and drop it directly into your SSP ghost's directory (ghost>shell>master) to enable the visual notification sign

### 4. (Optional) Swap the provided ringtone with a custom one

Download a .wav and place it in the ringtone folder, and rename it to "0271"

### 5. (Optional) Import your whole chat history (optional)

1. Use your phone to open whatsapp, and open your target's contact chat
   
2. click the three dots on the right and select Other > Export chat and choose 'with media'

3. If you choose a different name for your contact on config.json, go edit it to match how it's saved on whatsapp.

4. Use the import button next to the "Send" button on the UI, and wait - if you want to monitor the progress, you can do so by manually opening gui.py 
(Once done, you can now optionally change back your contact's name on config.json)

## Usage

### Launching the App
To start the application without keeping command prompt windows open, simply double-click the **`start_silent.vbs`** file. This script will:

- Detect your current installation directory.

 - Start the Node.js backend listener silently in the background.

- Wait two seconds, then launch the Python GUI (`gui.py`).

To have it run upon booting your pc, make a shortcut of start_silent.vbs (right click > show more options > create shortcut). 

Press Win+R and type shell:startup, you can now drop your shortcut in the folder that opens

### System Tray Controls

Once running, WA Ghost will appear in your Windows system tray. You can right-click the icon to:

Open the listener's event log.

Manually Show/Hide the desktop ghosts.
 
Safely Quit the application.
