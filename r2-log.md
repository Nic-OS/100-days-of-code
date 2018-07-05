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

### R2D13 - 5/21/18
**Goals:** 
  1) Successfully launch the camera
  2) Take a picture
  
**Results:** Achieved both goals! I launched the camera by importing and using the `<Camera />` component, which the react-native-camera docs mistakenly labeled `<RNCamera />` (probably from an older version). The node module Readme actually had great tips, and I basically copied the example code just to use the Camera component. My next step is to figure out how to use the picture I took in my API call to the computer vision API, which will let me scan the picture and extract the written text.

### R2D14 - 5/23/18
**Goals:** 
  1) Take and *store* picture
  2) Use picture in API call
  
 **Results:** I struggled to figure out how to save the picture I took. I combed through the documentation to see what the `.capture()` method included, but couldn't find anything. I saw some tutorials that had different version of saving the metadata and the uri, neither of which I understand. But then, I watched [this](https://www.youtube.com/watch?v=Ikgfr9Yot1M&t=313s) YouTube tutorial and realized that the pictures are automatically saved to the Camera Roll, and I could access them if I went to the Gallery on the emulator! I keep thinking that everything is transient on the emulator and therefore gets cleared after a while, but I have to consider the emulator as if it's a real phone. When I went to the Gallery, all the pictures I took were in there!
My next challenge is to launch the Camera view only after pressing a button. Right now, I tried:

```
render() {
    return (
      <View style={styles.container}>
        <Text style={styles.welcome}>
         Scan a new business card and watch the information populate below!
        </Text>
        <TouchableOpacity
          style={{height: 65, width: 95, alignItems: 'center', backgroundColor: 'blue'}} 
          onPress={this.launchCamera}
          >
          <Text>Scan new business card here</Text>
        </TouchableOpacity>
      </View>
    );
  }

  takePicture = () => {
    this.camera.capture()
      .then((data) => console.log(data))
      .catch(err => console.error(err));
  }

  launchCamera = () => {
    return(
        <Camera
          ref={(cam) => {
            this.camera = cam;
            }}
          style={styles.preview}
          aspect={Camera.constants.Aspect.fill}>
          <Text style={styles.capture} onPress={this.takePicture}>[CAPTURE]</Text>
        </Camera>);
  }
```
So that when I click the "Scan new business card" button, the Camera view launches, but it hasn't worked yet. I think I could get it to work with an if statement, though. But then I'll need to look into the whole async/Camera.ready/etc.

### R2D15 - 5/24/18
**Goals:** 
  1) Only launch camera when I press the `<TouchableOpacity/>`
  
**Results:** I successfully set it up so that the `<Camera/>` component only launched when I pressed the `<TouchableOpacity/>` button in my welcome screen. It took a lot of work, but I finally managed it by creating two separate components for each of the two screens: the welcome screen with the button and the camera screen. I then created a function in the main `<App/>` component that evaluated which screen component to render based on a boolean value (`isCameraLaunched`. To update that boolean value, I passed a function that changed the boolean value from false to true as a prop to the `<WelcomeScreen/>` component when the `<TouchableOpacity/>` was pressed. I also added a callback to the parent component by returning the newly changed state (`isCameraLaunched`). By initailizing `isCameraLaunched` to false, the component first renders the `<WelcomeScreen/>`. Then, when the button on the welcome screen is pressed, it updates the boolean to true and renders the `<CameraScreen/>` instead. I'm able to save pictures and look at them in the Camera Roll.
My biggest struggle to getting this to work was the syntax. I think I had a lot of issues with variable scope. I also unsuccessfully tried different variations of the if/then statement to render the different screens. I'm really pumped to have gotten this to work, finally!

### R2D16 - 5/25/18
**Goal:** Integrate REST API call into app.

**Results:** Spent the hour reading up on Firebase with React Native, but realized that was for backend stuff like user authentication. Tomorrow I'll look more into Google's Cloud Client Library.

### R2D17 - 5/26/18
**Goal:** 
  1) Add React Navigation via Stack Navigator
  2) Integrate REST API call into app
  3) Create new screen to display JSON data

**Results:** After adding the React Navigation and React-Native-Elements libraries, my project wouldn't build again. It kept running into dependency errors, I think. It's really annoying. I'm going to try to move the project to Expo to see if I can avoid those.

### R2D18 - 5/28/18
**Goal:** 
  1) Move project to Expo
  2) Add Navigation
  3) Make API call with Google Cloud Client Libraries
  
**Results:** I successfully moved the project to Expo but the Camera app wouldn't render anyway so I just ditched it. I don't have time to learn Expo-specific things when I know I'm going to change it later. I ended up having to start over **again** by deleting my app folder and initializing a new RN project because of dependency issues with the three third-party libraries I was using. 
After starting over, I installed the libraries first before adding any of my own code. I made sure to link them and run `yarn` again to get the node_modules up-to-date. Finally, it worked without a problem! So I added my code again (but created a separate Component folder) and added React Navigation as well. That easily solved my initial problem of only launching the Camera component `onPress`. Now, the button on the `<WelcomeScreen/>` component navigates to the `<CameraScreen/>` component.
Finally, I added some new color to the app, which I like a lot.

### R2D19 - 5/30/18
**Goals:** 
  1) Add Google Cloud Client Library for Vision API to project
  2) Figure out path of most recent photo captured to use in API call
  3) Set up API call to use path of most recently captured photo
  
**Results:**
  1) Set up Google Cloud Platform and installed the Cloud Client Library for the Vision API in my project.
  2) Still haven't figured out the path of most recently saved photo--will review react-native-camera documentation
  3) To set API call to use most recently captured photo, I'll have to use my actual phone for a development device.

### R2D20 - 5/31/18
**Goal:** Make API call when taking a picture using the photo path on disk.

**Results:** I added the code for the API call, but I still need a physical device to take a picture of the business card. I can't use mine because it's a Pixel 2 and has USB-C. The code returned an error when I ran it in the emulator just for kicks, but I feel burned out now so I'll have to look at it tomorrow. I'm excited about the progress today, though.

### R2D21 - 6/3/18
**Goals:**
  1) Analyze captured photo in API call
  2) Render results on `<ResultsScreen/>`
  
**Results:** 
  1) There seems to be an issue with using the gcloud services for the vision API with React Native. I had to comment out my API call to get the app to run. I'll continue looking into this.
  2) Although I couldn't render the results of the API call, I *was* able to `return` the path of the captured photo and log it to the console! That's exciting, because now I just need to figure out how to get the google API to play nice with React Native, then I'll be able to use the photo path in the API call.

### R2D22 - 6/5/18
**Goal:** Analyze a saved business card photo on the emulator and log the results.

**Results:** Didn't get it to work.

### R2D23 - 6/25/18
**Goal:** Move project to Expo and get the app to run on my phone through the Expo mobile client, while accessing the camera through the Expo SDK. 

**Result:** Success! I started using Expo and their Expo SDK--no more third-party library problems or dependency issues! I got the app to run, access the camera, and take a picture, but not display the results. Still working on that.

### R2D24 - 6/26/18
**Goal:** Render JSON data after taking picture.

**Result:** Haven't figured out how to structure the functions needed to capture, analyze, then render the photo data.

### R2D25 - 7/1/18
**Goal:** Rewrite functions to capture, analyze, and render photo data from the `<Camera>` component.

**Results:** I wasn't able to do it today. I feel like my lack of understanding some key JS concepts like Promises and async/await is really hindering me. It's hard to tell when to write a new function to handle a different action, when to link Promises, how to know when to use async/await, etc. At this point, I think I just have a lot of different bits of knowledge, but I lack a cohesive framework with which to understand everything. I have a lot more to learn about JS, that's for sure.

### R2D26 - 7/3/18
**Goal:** Break apart each step of the app's function to see which part isn't working correctly.

**Results:** Need to understand Promises better.

### R2D27 - 7/4/18
**Goal:** Break apart each step of the app's function to see which part isn't working correctly.

**Results:** Read a lot about promises and chaining promises. Will look into Await/Async functions tomorrow.

### R2D8 - 7/5/18
**Goal:** Learn enough about promises and await/async to break my `takephoto()` function up into separate parts to test each.

**Results:** Very close to a breakthrough! I tested each part of the function by logging the results to the console with Expo XDE. At this point, it says the body init of my `fetch()` request is an unsupported format; I'll have to look into that more. But, I'm making progress!
