# 100 Days Of Code - Log

### Day 1: January 1, 2018

**Today's Progress**: I learned more about managing state and props in React Native. I've [unsuccessfully] tried updating a method that sets the state based on the user input in the child component. I've corrected the syntax for the updater function in my setState method, but now the entire app re-renders when I call onSubmitEditing(), which still doesn't give me the result I want.

**Thoughts:** Even though I didn't really accomplish anything today, I'm getting a better grasp on managing state and props in React Native. I've been working on an app with a friend, which I'm using as a testing ground to learn to code. It's pretty obvious to me now that syntax is not difficult to learn; understanding the logic is what's difficult. I feel like I'm trying to think like a computer and understand how it would evaluate each statement, and in which order. I'm excited about the shift in my thinking/attention from just the syntax to what's actually happening behind the scenes. Looking forward to day 2.

**Link to work:** https://snack.expo.io/@nic-os/number-your-days

### Day 2: January 2nd, 2018

**Today's Progress**: I struggled through updating state again today. I understand the concept and can update state with setState, but just not <i>when</i> or <i>in the way</i> that I want yet.

**Thoughts:** My biggest issue comes with the onSubmitEditing method prop in my TextInput component. I can change the state easily enough with the onChangeEditing method, but something's not quite lining up when I do it with onSubmitEditing. The syntax seems to be right, but maybe I'm misunderstanding something about the relationship between parent and child components. I have the built-in TextInput onSubmitEditing prop in my child component (which is essentially just a TextInput component used to track the user's age) refer to a method in my main App component that sets the state ({userAge: ''}) to whatever the user typed. It doesn't seem to be updating correctly, though.

**Link to work:** https://snack.expo.io/@nic-os/number-your-days
