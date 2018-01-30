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


