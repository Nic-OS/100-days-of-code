# #100DaysOfCode Log - Round 2 - [Nico Salas]

The log of my #100DaysOfCode challenge. Started on [May 7, Monday, 2018].

## Log

### R2D1 
Starting a new app. Using Microsoft's Computer Vision API. Really excited to learn new skills for this app since it's very different from what I did in my first app. Reviewed JQuery and JSON/AJAX requests.

### R2D2
Practiced getting JSON data and converting to html. This will be a key feature of the app. Created Microsoft Azure account to use the Computer Vision API. Wrote a draft workplan for the app. I want to try hitting 2 hours of coding per day instead of 1.

### R2D3
Read through the documentation for the Computer Vision API. Tried going through the tutorial but couldn't get it to analyze an image.

### R2D4
Got the tutorial working. The problem was I didn't choose one of the few options in the API for a valid Subscription Region in my Azure dashboard, so the subscription keys weren't valid for me to use the API. I don't know why Microsoft even allows you to select regions that won't work with the REST API request later anyway.

I was able to have the API analyze my own business card and it extracted the text perfectly, though my next challenge will be to get it to properly classify what it's seeing (e.g., mobile number, fax number, email address, company name, etc.).

### R2D5-7
I've spent time looking at ways to validate the JSON data so that it detects whether it's an email, name, phone number, etc. I also started working with Firebase and MLKit to see if Google's solutions work better than Microsoft's. I've basically just been doing some tutorials and reading docs, but it's actually been very interesting to me.

### R2D8 - 5/12/18
**Goals:** 
  1) Start a simple app that instructs the user to scan a new business card.
  2) Figure out how to use the Camera in React Native
  3) Set the `onClick` prop for the button to open the camera and take a picture.

**Results:** Created simple app. Started watching tutorial on using the Camera in RN. Haven't set the `onClick` button prop to use the Camera yet since I don't know how. That'll be the next step for tomorrow.

### R2D9 - 5/14/18
**Goal:** Access the Camera in my emulator and a take a picture
  
**Results:** Installed `react-native-camera` but kept running into compilation issues. From what I can tell, it seems to be an issue between the versions of React Native and the camera library, but I can't figure it out. Spent a good two hours trying to get it to work to no avail. Going to take a break and try again later today.

### R2D10 - 5/15/18
**Goal:** Move project to Expo to avoid compilation errors. Get camera working and take picture.

**Results:** Moved to Expo but the camera still won't work. The documentation on the react-native-camera github page is crap, to be honest. It doesn't explain the props well and what's required to actually get it working, so I feel left to figure it out on my own by troubleshooting. I wish the docs were laid out like the Facebook RN docs.

### R2D11 - 5/16/18
**Goal:** Get camera working by any means necessary.

**Results:** Got confused about actually using the Camera component because I kept seeing these `.then` methods in the code. Spent the hour reading up on Promises from this awesome article by Brandon Morelli: https://codeburst.io/a-simple-guide-to-es6-promises-d71bacd2e13a. Hopefully by breaking down the different components of using the `Camera`, I'll actually be able to use it and not get tons of errors every time.

### R2D12 - 5/18/18
**Goal:** 
  1) Get camera working on emulator
  2) Take and store picture on device storage
  
**Results:** It took me longer than the full hour just to get the app to compile with the right dependencies and run on the emulator. I haven't even actually used the Camera component yet. I had to keep installing, then linking, then unlinking, then uninstalling, then reinstalling, etc. the `react-native-camera` library. Finally, I just deleted the entire project and created a new React Native project to try again completely fresh. It finally worked. So now, I at least have the `react-native-camera` library installed and linked to the project and can run the app on the emulator. Tomorrow, I'll try using the camera component.
