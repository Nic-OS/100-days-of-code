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
