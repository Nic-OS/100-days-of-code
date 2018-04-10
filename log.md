# 100 Days Of Code - Log

### Day 1: January 1, 2018

**Today's Progress**: I learned more about managing state and props in React Native. I've [unsuccessfully] tried updating a method that sets the state based on the user input in the child component. I've corrected the syntax for the updater function in my setState method, but now the entire app re-renders when I call onSubmitEditing(), which still doesn't give me the result I want.

**Thoughts:** Even though I didn't really accomplish anything today, I'm getting a better grasp on managing state and props in React Native. I've been working on an app with a friend, which I'm using as a testing ground to learn to code. It's pretty obvious to me now that syntax is not difficult to learn; understanding the logic is what's difficult. I feel like I'm trying to think like a computer and understand how it would evaluate each statement, and in which order. I'm excited about the shift in my thinking/attention from just the syntax to what's actually happening behind the scenes. Looking forward to day 2.

**Link to work:** https://snack.expo.io/@nic-os/number-your-days

### Day 2: January 2nd, 2018

**Today's Progress**: I struggled through updating state again today. I understand the concept and can update state with setState, but just not <i>when</i> or <i>in the way</i> that I want yet.

**Thoughts:** My biggest issue comes with the onSubmitEditing method prop in my TextInput component. I can change the state easily enough with the onChangeEditing method, but something's not quite lining up when I do it with onSubmitEditing. The syntax seems to be right, but maybe I'm misunderstanding something about the relationship between parent and child components. I have the built-in TextInput onSubmitEditing prop in my child component (which is essentially just a TextInput component used to track the user's age) refer to a method in my main App component that sets the state ({userAge: ''}) to whatever the user typed. It doesn't seem to be updating correctly, though.

**Link to work:** https://snack.expo.io/@nic-os/number-your-days

### Day 3: January 10th, 2018

**Today's Progress**: Although my family and I just moved to a new city, which was last-minute and didn't leave much time for coding, I've gotten back into my 100 Days of Coding challenge. Today, rather than jump back into my React Native project, I spent the time updating a simple website for my wife.

**Thoughts:** It was a little discouraging to miss a little over a full week of coding right from the start of this challenge, but we found out about our move a week before the move-in date (applied and got approved for the apartment we wanted, but the move-in date was a firm Jan. 5th at our price point), and then had to frantically clean, pack, and move all by ourselves (my wife and I). It was rough.

However, now that we're all moved in, we're loving our new place and I'm excited to code more this year! I got back into it tonight by doing some relatively simple things. I spent some time working on the Tribute Page for my wife, which is a Free Code Camp project I'd put off because I thought it was too easy. That was actually nice because I hadn't done any basic HTML/CSS in a while, so it was pretty fun. Everything seems like it clicks so much better after you take a break then come back to it later. Tomorrow I'm getting back to the React Native project.

**Link to work:** https://codepen.io/Nic-OS/pen/JNOZdq
                  https://snack.expo.io/@nic-os/number-your-days
                  
### Day 4: January 11th, 2018

**Today's Progress**: I think I'm starting to understand the different ways (probably on a simple, conceptual level) to update the state. I've tried different ways to do it and I <i>think</i> I finally got it....maybe.

**Thoughts:** The problem is that my component re-renders completely and resets the state, so I haven't figured out how to check if the state is actually updated when the onSubmitEditing method is called but then reset during the re-render, or if I'm just not successfully updating the state at all. I've inserted some simple text in the component View to check if the state is updating (something like: "The state is now: " {this.state.userAge}), but it never updates with the number I've inserted in my input component. *sigh*.

Still, I'm super excited to be coding again! This is the main thing I want to learn this year!

**Link to work:** Same old, same old -- https://snack.expo.io/@nic-os/number-your-days

### Day 5: January 12th, 2018

**Today's Progress**: I cleaned up the code in the app by getting rid of some things I added in the beginning but realized I didn't need. I added some Text to help me track whether the state was really being changed and when.

**Thoughts:** I felt really good about cleaning up the code a bit. As a beginner, it can be scary deleting things cause you don't understand why it needed to be there in the first place, and you expect the whole app to crash. I'm encouraged that I'm starting to understand enough to know what I don't need. 

However, I had to reach out to a friend to finally break through this wall with changing the state. I think I'm not understanding something about passing data between parent and child components. Right now I have the child component's onSubmitEditing prop just call a function that should update the user's age based on the input. The onChange function works fine and seems like a simple, shallow merge of the new state and old state. However, when I call setState for onSubmitEditing, it still re-renders the entire app and doesn't update the state at all. I'm really hoping my friend will help me break through this part because I'm sick of slogging through the same problem everyday.

**Link to work:** https://snack.expo.io/@nic-os/number-your-days

### Day 6: January 13th, 2018

**Today's Progress**: Made two new simple React Native snacks on Expo to test how to better use a TextInput component.

**Thoughts:** I'm still struggling with updating the state in my app. I've copied other examples almost to the letter (other than changing the names of the functions/variables) and it'll work just fine in the examples but not in my app. I created two new simplified apps that do nothing except update state through a TextInput component. I'm trying to simplify things as much as possible so I can understand the basics of what's happening and why it's not working in my main app. The good thing about this struggle is that I know I'm going to learn core principles of how and why things work; I won't just copy someone else's code and pretend I came up with it in my own app. I actually want to understand all this stuff, not just "make it work."

Also, when creating the two simple snacks on Expo, I was able to write a lot of the code from memory. That's encouraging to me because I'm excited to know the syntax so well that I can focus all my attention on the actual logic of the app. Looking forward to tackling it again tomorrow.

**Link to work:** https://snack.expo.io/@nic-os/number-your-days

### Day 7: January 14th, 2018

**Today's Progress**: I successfully updated the state!!! I got it to work after carefully comparing the syntax from several different examples of passing data between parent and child components. Now, whenever I enter the user's age in the TextInput component and click submit, the state containing the user's age updates and displays.

**Thoughts:** Honestly, I still don't really understand how it works. I copy and pasted some code from an example (I know, but it was just a test to see if I was somehow doing something wrong that I wasn't noticing) and it worked. That really confused me because I thought I'd already meticulously copied the parts that were relevant to my app. I changed the function and variable names and so on but it just would not work for me. It kept re-rendering the component every time and not updating the state. I'm going to keep looking into it, but I'm happy it works now. Hopefully, now I can work backwards and try to figure out why it works now when it didn't before. I actually want to understand this stuff on a deep level; I don't just want to copy code.

**Link to work:** https://snack.expo.io/@nic-os/number-your-days

### Day 8: January 15th, 2018

**Today's Progress**: I began playing with updating the state of a new input component, which is a Picker component, for another aspect of my app. I was able to successfully update the state to what I wanted, but only within the child component, not the parent component.

**Thoughts:** The more I learn about React Native, the more I see that probably the most important thing to master is the exchange of data and manipulating state between parent and child components. At this point, it seems to me that if you can do that <i>really</i> well, the other things are much more straightforward. Having function props pass data between parent and child components can be tricky to keep track of and understand. I think I should invest the most amount of time and energy in really getting this down.

**Link to work:** https://snack.expo.io/@nic-os/number-your-days

### Day 9: January 16th, 2018

**Today's Progress**: I drew a flow chart to help me trace the logic of the app and exchange of data between the parent and child components. I felt like I needed to visualize it to really grasp it. As I said yesterday, I keep getting the sense that managing state between parent and child components is essential to using React Native properly, so I'm committed to really getting the hang of this. I also made some changes to my next input component, which is a Picker component. By the end, though, all I'd managed to do was get my app to crash every time I opened it lol.

**Thoughts:** Even though I ended my hour of coding with my app repeatedly crashing every time I opened it, I feel encouraged! I actually feel a lot less intimidated every time I sit down to code. I used to be intimidated and it made me want to avoid coding, which led to all kinds of excuses to get out of doing it (even though I really wanted to code). Now, I feel pretty comfortable with the old Facebook motto: "Move fast and break things." I definitely broke my app tonight lol. Looking forward to tomorrow!

**Link to work:** https://snack.expo.io/@nic-os/number-your-days

### Day 10: January 17th, 2018

**Today's Progress**: This was one of my less productive days. I experimented with a few different ways of passing data from my Picker child component to my main App parent component, but I couldn't get it to work quite like I wanted. I moved my project from Expo back to Atom because I was getting weird errors in Expo.

**Thoughts:** Tonight, I considered it a victory that I even sat down to code. It was one of those nights where I was exhausted but refused to go to sleep without coding. I didn't accomplish much, but I at least reviewed my code, walked through some things I did yesterday and experimented with things I wanted to try tonight. I'm very happy about just overcoming Resistance tonight and sticking to my commitment to doing this thing I really care about.

**Link to work:** https://snack.expo.io/@nic-os/number-your-days

### Day 11: January 18th, 2018

**Today's Progress**: Spent some time practicing React building simple web pages.

**Thoughts:** Although I didn't do any real work on the app, I feel like I've kind of started to forget basic JS and React concepts as I struggle through React Native. When I encounter an error, I'll look into it and realize that it was a relatively simple concept that I forgot about, such as the limitations of block-scope variables. So, I spent some time refreshing tonight by creating some simple web pages with React and following a tutorial to brush up on some basic skills.

**Link to work:** Nothing really to show here tonight, unfortunately.

### Day 12: January 19th, 2018

**Today's Progress**: I got almost every one of my child components to work correctly!! I added a few things to make sure the parent component's state was updating properly, but I did have some issues with those.

**Thoughts:** I feel so much happier about coding now. It's amazing how solving a problem can completely change your attitude toward coding.

### Day 13: January 20, 2018

**Today's Progress**: Got my userGender component to update the parent state. 

**Thoughts:** I'm loving working on this app.

**Link to work:** https://snack.expo.io/@nic-os/number-your-days

### Day 14: January 22, 2018

**Today's Progress**: I completed the basic functionality of my app!! I got all child components to correctly update the state by providing a callback to the parent (prop) within the child component's primary function. For my TextInput component, it was the onSubmitEditing prop. For my Picker components (userGender and userCountry), it was their onValueChange prop. I added a function that my friend showed me that displays the state attributes as they're updated, so I could make sure the callbacks between parent and child components were actually working--they do!!

**Thoughts:** I was so excited to complete this part of the app. I've been working on it for a long time and there were several points where I was stuck for weeks. I missed coding yesterday but hit it hard today and it paid off! I just kept troubleshooting and asking myself, "Okay, why isn't this particular thing working? It seems to be written exactly like the other component, which is working, but for some reason <i>this one</i> isn't working--why not? What's different?" And that led me to figure out that I wasn't passing the user's inputted value (in the child component) as an argument to the function prop. Therefore, the parent component couldn't access the value from the child component that it needed to update its state. Now all that's left is tweaking some things and updating the UI!

**Link to work:** https://snack.expo.io/@nic-os/number-your-days

### Day 15: January 23, 2018

**Today's Progress:** Added React Navigation to the project. Adding a separate page for each component. Trying to commit the local repository to GitHub so I can start tracking versions as I change the UI. 

**Thoughts:** I'm really excited to learn Git and GitHub now. It seems like it'll make things so much easier, plus it'll allow me to contribute to other open-source projects once I gain more skills. I love the idea of being a part of the open-source world. Using Git has given me a sense of being connected to other developers and their projects beyond my own simple apps. As far as my own current app, I think (hope) I'll be done with it by next week!

**Link to work:** https://snack.expo.io/@nic-os/number-your-days (trying to add the local repository to GitHub but still learning that part :D)

### Day 16: January 25th, 2018

**Today's Progress:** Still working through using React Navigation. I created a simple test app to practice with before I add it to my app.

**Thoughts:** I missed a day yesterday, which was discouraging, but I don't want to lose any steam! I still want to code as much as possible. I know I just need to focus on consistency.

### Day 17: January 26th, 2018

**Today's Progress:** I went back to my FreeCodeCamp Tribute Page (which I still need to finish) and tried changing some things, mostly formatting and content.

**Thoughts:** Going back and forth between programming languages can be a bit confusing but can also make things easier. React Native has a lot of similarities to HTML/CSS, at least in terms of my conceptual understanding of it. An obvious example of this is the similarity between divs and Views. I'm liking that continuity.

## Day 18: January 27th, 2018

**Today's Progress:** Struggled through some more React Navigation stuff, as well as continuing to learn about Git and GitHub. I didn't add React Navigation to my main app yet, just changed some things in the test navigation app to get a better understanding of how it works and how I would integrate it into my app.

**Thoughts:** I almost wish I would've tried learning React Navigation from the get-go so that it would be easy to integrate into my existing app. Then again, I think I needed to focus on just the basics in the beginning, step by step. Although Navigation seems a bit confusing right now, I think that's also partly because I haven't had the best opportunities to code this week with a 1 year old.

## Day 19: January 28th, 2018

**Today's Progress:** Going through some tutorials with React Navigation made it even more confusing, so I've also been reading through documentation as I change things here and there in the test app. Do I add the Stack Navigator to each child component? Or do I add the Stack Navigator to the main App component and pass the child components in there as the 'screen'?

**Thoughts:** I think I can actually finish this app this week, as long as I can get a good hour in each day (with no interruptions or distractions!).

**Link to work:** https://github.com/Nic-OS/number-your-days

## Day 20: January 29th, 2018

**Today's Progress:** Pretty much just read through a lot of documentation today... I'm *definitely* going to make awesome progress on the Stack Navigator tomorrow. 

**Thoughts:** My hour coding every day hasn't been very productive the last week, so that's a bit discouraging, but I'm not giving up. I'm counting it a success if I just sit down and code regardless of the outcome. The more I'm exposed to the material and practice, the better I'll be.

**Link to work:** https://github.com/Nic-OS/number-your-days

## Day 21: January 30th, 2018

**Today's Progress:** I didn't really accomplish anything today other than more reading, which I didn't understand.. *sigh*.

**Thoughts:** For some reason, React Navigation has been hard for me to understand conceptually, at least as far as how to integrate it into my existing app. I keep running into the same issue of whether I should add the Stack Navigator to the main App.js file or to each of the child components, which I would then render in the Stack Navigator.

**Link to work:** https://github.com/Nic-OS/number-your-days

## Day 22: January 31th, 2018

**Today's Progress:** After trying to integrate Navigation into my app, I saw a *looootttt* of error messages. I almost feel like starting from scratch so that I can use what I've done but with React Navigation specifically in mind. I did finally move from just reading documentation to actually coding today, so that was awesome.

**Thoughts:** I've felt like React Navigation put me in sort of a slump the past week or two. I lost a lot of motivation to code because it seemed confusing and frustrating. Tonight, I forced myself to just *try* things and code. As a result, I got nothing but errors every time I re-rendered, but it was the most exciting time coding I've had for weeks now. The challenge made me not want to stop and I coded for two hours instead of one tonight. I'm super pumped to try again tomorrow morning with coffee :D

## Day 23: February 1st, 2018

**Today's Progress:** I can't seem to integrate the Stack Navigator into my app as smoothly as I planned. My main issue is that I can't figure out the best way to render the Stack Navigator. I learned that every class-based React component needs a Render function, but for some reason the Stack Navigator didn't render when I tried passing it in. I could've just written it wrong, but it threw me off. I tried changing my App component to not be a class-based exponent, but instead just having the Stack Navigator be the default export of the App.js file so that *that* was rendered instead--it didn't work. 

**Thoughts:** I'm a little discouraged that this has been so hard to grasp. I feel like learning new things in React Native has been a lot harder than I expected. I seem to always spend more time learning than I'd like. I expect that I should be able to pick things up quickly--at least no more than a day or two before I can start using them. It just doesn't happen for me, though. I try not to spend too much time reading documentation and instead just get into coding, but then I inevitably get stuck and need to go read the documentation anyway. Honestly, this whole project app has taken longer than I wanted it to, but I'm happy to make even a little progress every day.

**Link to work:** https://github.com/Nic-OS/number-your-days

## Day 24: February 3rd, 2018

**Today's Progress:** I tried changing a few different things to get the Stack Navigator to render but I kept getting errors. Most of them said my app wasn't registered, so I tried making small syntax changes but those didn't work. I have another copy of the app in Expo which I've used to compare. Tomorrow I'm going to try just rendering the Stack Navigator in the main App render function again. I'm just going to store the Stack Navigator in a variable in the main App.js file, pass in each child component as screens after storing the configured components as variables, then render just the Navigator.

**Thoughts:** Still determined, need to keep trying things. I've felt so tired the past few days, but I'm still counting it a win if I can just manage to code for an hour. I missed yesterday and forced myself to code tonight. As long as I make progress!

**Link to work:** https://github.com/Nic-OS/number-your-days

## Day 25: February 4th, 2018

**Today's Progress:** I have the Stack Navigator added to my app and can render it, but my main problem is finding the best way to pass props to the child components. Before I added Navigation, I could just pass data to the props of the child components when I rendered them in my main App.js component. Now, I can't find a functional way to do that while the child components are in the Stack Navigator. 

**Thoughts:** After seeing so many error messages the past few days, I've tried to consciously react to problems as puzzles to be solved instead of something to get frustrated about. Ideally, I want to develop a joyful persistence because I know coding is going to be full of problems. As far as what I need to do in my app now, I read a thread on GitHub where someone had my exact same issue (passing data to props in the child components without going through the Stack Navigator `this.props.navigation.state.params`). If I can figure that out, I should be completely done with **all** the functionality of the app, and I can completley focus on UI stuff, which I'm really excited about. My goal for this week is actually to code for *more* than an hour a day. Basically, I want to use all my free time to code. I think I need to just immerse myself in this stuff at this point. I want to get good at coding, and I know that requires complete immersion.

**Link to work:** https://github.com/Nic-OS/number-your-days

## Day 26: February 5th, 2018

**Today's Progress:** I didn't really make any progress today. I found a potential workaround to the issue of passing regular props to child components instead of navigation params [here](https://github.com/react-navigation/react-navigation/issues/935). I still can't find a workable way to pass the props I need to the child components when I'm using navigation.

**Thoughts:** When this was a single page app, I could easily just have separate child components that were merely presentational and one container component (App.js). I wrote functions for each child component and passed them as props when rendering them all in the main App `render()` function. Now, I don't know how to pass those same functions as props to the child components when using them in the Stack Navigator. The thing that really confuses is what the structure of the app should be. It seems that the Stack Navigator should be a separate component, but then what about the App logic and data? Where should I store that? In the App component? Okay, but then how do I access the main app data when I'm configuring the Stack Navigator? I think I need to move things around somehow. I again moved the project to [Expo](https://snack.expo.io/@nic-os/number-your-days) so I could get feedback in real-time when I have errors.

**Link to work:** https://github.com/Nic-OS/number-your-days

## Day 27: February 8th, 2018

**Today's Progress:** I tried implementing the solution that others suggested to pass navigation params to props. I initialized the Stack Navigator in the main App component, then used a function to create a wrapper for each screen component so that I could map the navigation params to props without having to rewrite the code for each of my child components. I haven't quite gotten it to work yet, but I think I'm on the right track.

**Thoughts:** The confusing part for me is how to pass functions in the params/props where I'll need a callback to the parent component. Before using Navigation, I could simply call each child "dummy" or "presentational" component and pass functions as props to them, which would allow me to access the data they were capturing and store it centrally in the state of my main App component. That was a good solution because I could keep almost all of the app logic in the main App component. Now, it seems like I'll have to rewrite at least *some* code in each child component if I want to pass props to each. But even then, how will I pass the functions I wrote in the main App component and access the data from each child component to store in the App component? That's the part that's really stumping me. 

**Link to work:** https://github.com/Nic-OS/number-your-days

## Day 28: February 9th, 2018

**Today's Progress:** I actually got the Stack Navigator to work!! It actually renders something on the screen! I still need to fix the params/props issue so that each screen has what it needs to properly render and function, but at least I have the core issue resolved.

**Thoughts:** I kept getting an error after adding the `const RootNavigator = StackNavigator()`, but I realized it was because I had it in the wrong place. I had it within the `export default class App extends Component{}`, but outside the `render()` function. So once I added it like this:

```
export default class App extends Component {
...
render() {
const RootNavigator = StackNavigator(...);

return <RootNavigator />;
 } 
}
```

It worked fine! I also had to fix tiny syntax errors that kept throwing me off, like not capitalizing the `title` prop in my `Button` component. So now, I have to figure out the best way to pass props to my presentational components with react navigation. I'm excited to be done with this simple project that's taught me so much about React/React Native and coding in general!

**Link to work:** https://github.com/Nic-OS/number-your-days

## Day 29: February 10th, 2018

**Today's Progress:** I am happy to report that the Stack Navigator is fully functional! It looks ugly and the last component doesn't work yet (calculating remaining days), but the navigator itself is all done!

**Thoughts:** I'm so happy to have gotten the Navigator to work. The feeling of reloading your virtual device and not seeing a red error page is indescribable. There was a point where I was just cranking out `Button`s and editing all the presentational components as if it were automatic, and I felt really good. I'm such a newbie, but I've learned so much that I can't help but be proud of how far I've come. I don't think the final component will be nearly as difficult as figuring out React Navigation in general. I get the sense that I've passed a really important checkpoint, and it's all downhill from here.

**Link to work:** https://github.com/Nic-OS/number-your-days

## Day 30: February 11th, 2018

**Today's Progress:** I made some minor UI changes to center the `View`s for each component, enlarge and bold the `Text`, etc. 

**Thoughts:** I was feeling tired today so I didn't want to frustrate myself trying to tackle any large problems. Still, I wanted to make the most of my time so I at least made some UI changes that I knew I'd have to get to eventually. Tomorrow I'll get back to figuring out how to finish the last component. The last issue left is storing and accessing the app's data in the `<DaysLeft />` component.

**Link to work:** https://github.com/Nic-OS/number-your-days

## Day 31: February 12th, 2018

**Today's Progress:** After attempting a few different ways to pass data as params from the main `<App />` component to each presentational component screen in the Navigator, I concluded I need to learn and use Redux for this app. I don't think there's an easy way to do what I need to do. And, even if I did figure it out, I don't think it would be best coding practice. I get the sense it would be more of a workaround but not actually good code. So, I started reading up on Redux today as well.

**Thoughts:** I'm glad I tried using params to pass data first because I think it was good practice for me. I knew I'd eventually need to learn Redux but was hoping to finish this app without it. From the little I know of it, it definitely seems like the solution to my problem of accessing app data across the whole app. So, on to Redux!

**Link to work:** https://github.com/Nic-OS/number-your-days

## Day 32: February 13th, 2018

**Today's Progress:** Installed Redux and React Redux in my app. Still learning how to properly integrate it.

**Thoughts:** I'm pretty much just reading documentation and watching a few tutorials on using Redux at this point. The difference between Actions and Reducers is the most confusing part for me right now. I don't see why you can't just have a Reducer function that modifies the state in some way on its own. Having Actions and Reducers just seems like destructing the process in an unnecessary way, but I'm sure I'll learn more about why it's important later.

**Link to work:** https://github.com/Nic-OS/number-your-days

## Day 33: February 15th, 2018

**Today's Progress:** Created reducer folder with index file and reducers for each property of my app's state. Moved all app data to the Redux reducers.

**Thoughts:** I really enjoyed coding tonight. I watched some course videos on Redux and read through some documentation while adding my own reducers. Using Redux seems like *such* a better system for managing app data, even for smaller apps like mine. It just feels a lot more organized and simple. It can definitely be a little confusing trying to track the flow of data throughout the app when you have so many different files and components floating around, but once you successfully integrate them it helps to have them compartmentalized. I almost didn't want to stop tonight! Already looking forward to tomorrow.

**Link to work:** https://github.com/Nic-OS/number-your-days

## Day 34: February 17th, 2018

**Today's Progress:** Reviewed reducers, used the `connect` function in react-redux to mapStateToProps in order to access the global state from within my UserAge component.

**Thoughts:** Reducers make sense to me, but I can tell this is where it's going to get more confusing. Usually I've had to review the same concepts 2-3 times to really have them stick, so I expect to do that soon when starting Actions and ActionCreators.

**Link to work:** https://github.com/Nic-OS/number-your-days

## Day 35: February 19th, 2018

**Today's Progress:** Started learning about ActionCreators, created my own for the UserAge component and used the `bindActionCreators` function to map the ActionCreator `setUserAge` to `this.props.onSubmit`. 

**Thoughts:** I didn't feel very focused this morning, probably because I've missed coding two of the last three days. I'll probably review ActionCreators and Actions later tonight again to try and have it stick before (hopefully) advancing tomorrow. I'm not quite sure what or if there's a difference between Redux for React vs. React Native, but I've been following a model from a tutorial on React, so I hope it's not too different. Either way, I still feel like I'm in the learning phase, so I don't mind going back and changing something to make it better because it'll help me learn more thoroughly anyway.

**Link to work:** https://github.com/Nic-OS/number-your-days

## Day 36: February 23rd, 2018

**Today's Progress:** Started off with reviewing the ActionCreators again since I'd missed a few days. I made some minor updates and deleted some things that were unnecessary or overly complex.

**Thoughts:** I'm disappointed that I missed a few days. I think it was easier to skip because it's difficult learning something new, which is what I've been doing the past few coding sessions. There have been several stages where I thought I was close to being done with the app and then I had to learn something new (i.e., Navigation, then Redux). I'm grateful that I've been learning so much, though. I need to focus on the process of learning and growing, not necessarily on any particular outcome, although I am obviously shooting for completing this app.

**Link to work:** https://github.com/Nic-OS/number-your-days

## Day 37: February 25th, 2018

**Today's Progress:** I updated my code to have each component rely on the actions and reducers to manage state. Initially, I began with managing all state in the App.js file, but I also had local state for each presentational component that I then passed back to the parent component. Now I've gotten rid of the local state so that only the actions manage the global state. However, I'm still able to render the current global state within each presentational component since I mapped state to props.

**Thoughts:** Things are really "clicking" for me now. I'm actually enjoying learning and using Redux. I've been a little scared to actually run my app in the simulator for fear of rampant errors lol, but I'll run it after I *think* I'm completely done setting everything up. At this point, I know there will be many errors. One thing I'm excited about is that, as I review this Redux stuff and trace the flow of data, I can visualize it in my mind and that's really been helping to connect the dots. The big breakthroughs come for me when I'm able to visualize what I'm doing and why. Hopefully I make great progress this week!

**Link to work:** https://github.com/Nic-OS/number-your-days

## Day 38: February 27th, 2018

**Today's Progress:** Cleaned up some minor errors in the ActionCreators.

**Thoughts:** Got all ActionCreators almost completely set up. It's been kind of a lot to keep track of, and I keep feeling like I should add more comments to my code, but I'll go back and add comments at the end when I actually get it working.

**Link to work:** https://github.com/Nic-OS/number-your-days

## Day 39: February 28th, 2018

**Today's Progress:** I got everything set up with Redux and navigation! All ActionCreators, reducers, the StackNavigator--everything! I completely rewrote the App.js file so that it was only a presentational component for each of the container components and the RootNavigator. The complete functionality (including full state management through Redux) should be *almost* fully done.

**Thoughts:** I tried running the app in the simulator but got weird, undecipherable errors. So, I moved everything to Expo (again) so that I could get more detail on the errors. Oddly, there were none, and when I ran the app in the Preview simulator, it actually rendered my Welcome Screen. However, when I clicked the button to begin and advance to the UserAge component screen, the app re-rendered and started over at the Welcome screen. It's hard to tell why exactly, but I have a feeling it has to do with the state starting off null and then updating to cause a re-render. I'll have to figure that out.

**Link to work:** https://github.com/Nic-OS/number-your-days; https://snack.expo.com/@nic-os/number-your-days

## Day 40-43: March 1st, 2nd, and 5th

**Today's Progress:** I've been stuck trying to get my app to render properly. I think I configured Redux incorrectly, though I followed a tutorial pretty closely and only modified it for my particular app. I didn't actually create a Redux `store` to pull from, but I generated the app state by returning it from the reducers, which might be why it hasn't loaded properly.

**Thoughts:** I'm ready to be done with this app. I've already spent way too much time on it than I should have, and it really should've only taken me a weekend to do it. It's taken me FOUR MONTHS. Granted, I'm learning as I go, but still, it's not complicated at all and should have worked much sooner. Tomorrow I'll try setting up my Redux store and will change things around a bit. I've been using [React Native Express](www.reactnativeexpress.com) to reevaluate my Redux setup, and I think I'll use that as a template for my own app. I desperately want to be done with this app as soon as possible so I can move onto something more fun.

**Link to work:** https://github.com/Nic-OS/number-your-days

## Day 44-45: March 7th, 8th

**Today's Progress:** 
March 7th was pretty unproductive. Figuring out how to restructure Redux. Different tutorials are saying different things and setting them up differently, so I've gotten pretty confused. 
March 8th was more productive. Today I've actually restructured Redux and am following the official Redux documentation (seems obvious). The only thing I haven't done yet is set up my `store`. I also combined all my reducers into one file and my action creators into one file for simpler organization. I previously had my folders and files set up as if it were a complex app, which it's not, so it made navigating through the files unnecessarily difficult. I hope this streamlines things. 

**Thoughts:**  One thing I've noticed is that tutorials often do things a certain way *assuming* either a complex or simple app. For instance, you may organize Redux differently for your app if it's large and handles a lot of data vs. a simple app (like mine) that doesn't have a lot of data to manage. When I follow tutorials that assume a complex app, things don't make sense to me and seem overly complicated, which is confusing. Now that I've cleaned things up a bit, I realize how dramatic the difference is between "clean" and "messy" code. I'm glad I'm not just making things *work*, but hopefully make them work *well*.

**Link to work:** https://github.com/Nic-OS/number-your-days

## Day 46: March 16th, 2018

**Today's Progress:** I *hopefully* simplified my app further by just having one reducer for the app, as opposed to a separate reducer for each piece of state. I know it's better to separate reducers, but I think my app is so small and simple that one reducer is just easier at this point. The one reducer only needs to update the state via a switch statement as it evaluates the action type and updates the piece of state accordingly. I also created the Redux `store`. 

**Thoughts:** I fell off the bandwagon for quite a while, but I'm back to it now. I let lack of sleep keep me from attempting to code by telling myself I was too tired to learn/practice. I'm eager to test my app and I really hope I can get everything working. I have two weeks of productivity coming up, so my goal is to have the app completely done by then. Tomorrow I'll focus on passing the Redux store to each container component in order to let each access and update the store.

**Link to work:** https://github.com/Nic-OS/number-your-days

## Day 47: March 20th, 2018

**Today's Progress:** I fixed some navigational things that were throwing me off for a while because I didn't realize what I was doing wrong. 

**Thoughts:** I think the only remaining challenge is understanding the best way to connect or "pass" my store to the rest of my container components. I've previously just copied tutorials, which led not only to me not understanding, but to the app not working anyway! I've been learning Redux slowly, but it's because I really want to understand why things are set up the way they are. I just want to finally get a working app going.

**Link to work:** https://github.com/Nic-OS/number-your-days

## Day 48: March 24th, 2018

**Today's Progress:** I passed the `store` to all components by passing it to the `Provider` component in Redux, then rendering `App` within the `Provider` component, like so:
```javascript
let store = createStore(rootReducer);

const AppWithStore = () => (
  <Provider store={store}>
    <App />
  </Provider>
)
```
It feels good to finally be done passing the store to all components, which held me up for a while.

**Thoughts:** To my great delight, I did not get the red error screen of death when I tried rendering my app in the simulator. Navigation worked as expected. The only problem was that the final screen, which is my `DaysLeft` component, did not show the number of days left. I don't know where exactly the issue is, though. I'll have to investigate whether the `store` is actually updating at all, or if it's specifically something in the `DaysLeft` component calculation. Still, I made great progress today and am very excited.

**Link to work:** https://github.com/Nic-OS/number-your-days

## Day 49: March 31, 2018

**Today's Progress:** FUNCTIONALITY IS FINALLY **DONE**!! I actually got everything working as it should be. I think the problem was that the action creators were not properly dispatching to the reducer. I had to rewrite them from what I found in a tutorial a while back to what was in the official Redux documentation.

**Thoughts:** It feels so good to actually be done with this. I'm going to do some minor UI changes to make it not look like crap, then I'll be done with it. I'm ready to move on to other projects ASAP. I lost motivation for this one a long time ago since it was supposed to only be to help me learn React Native, but it ended up taking longer than I expected. My goal is to be completely finished by this weekend!

**Link to work:** https://github.com/Nic-OS/number-your-days

## Day 50: April 3rd, 2018

**Today's Progress:** Added some styling to the initial Welcome screen.

**Thoughts:** Now that I'm completely focused on styling, it's like learning something new all over again! I haven't focused on styling/CSS for several months now since I only wanted to fix the functionality. Now, this feels really fun because I'm not worried about making a mistake. If I do something wrong, my whole app doesn't crash; it only affects the layout of the components. 

**Link to work:** https://github.com/Nic-OS/number-your-days

## Day 51: April 4th, 2018

**Today's Progress:** Added styling to the Age input screen.

**Thoughts:** I'm really having fun with the styling. I'll just do some basic styling and then move onto the next project.

**Link to work:** https://github.com/Nic-OS/number-your-days

## Day 52: April 6th, 2018

**Today's Progress:** Minimal styling changes. Added better comments throughout app to keep track of what's happening.

**Thoughts:** Today felt like an "administrative" day, but it really helps me to understand what I've done. It felt good commenting throughout the app, particularly for React-Redux things.

**Link to work:** https://github.com/Nic-OS/number-your-days

## Day 53: April 7th, 2018

**Today's Progress:** Moved all styling to a stylesheet to clean up the code. Added a `KeyboardAvoidingView` and `Keyboard.dismiss()` to improve the user experience.

**Thoughts:** These kinds of small changes feel good because they're simple. It's a nice way to finish up the app with simple polishing touches.

**Link to work:** https://github.com/Nic-OS/number-your-days

## Day 54: April 10th, 2018

**Today's Progress:** `<TouchableWithoutFeedback onPress={Keyboard.dismiss}` wasn't working initially, but that's because I had everything wrapped in the `<KeyboardAvoidingView>`, which I couldn't get to work no matter what I tried. So, I just deleted it and kept the `<TouchableWithoutFeedback>` component. It's working now!

**Thoughts:** It's so funny how seemingly minor things can take up so much time. I've set a hard goal for myself to finish the app by this weekend.

**Link to wrok:** https://github.com/Nic-OS/number-your-days
