# Lab Report 2

## Part 1
I used the same methods from class that were used during the labs (add numbers URL one) and changed one of the methods to add strings together using StringBuilder and append. It will try to locate the term "/add-message" in the URL, if it doesn't find any strings after it will just return the "404 Not Found!" as an error message. If the /add-message is found in the URL with the strings following it will update "Stringer" by appending the words. Lastly, it will return Stringer as a response and appear on the page.
![Image](Screenshot 2023-11-05 at 5.19.15 PM.png)
Next, I tested by using the example that was given to me in the lab report which was "/add-message?s=Hello" in which it printed the statement "Hello" correctly

![Image](Screenshot 2023-11-05 at 4.54.23 PM.png)
![Image](Screenshot 2023-11-05 at 4.54.27 PM.png)\n

It checks the /add-message using the code line "if (url.getPath().equals("/add-message"))" then with the next line "String message = url.getQuery();" it will grab the message that you want to add. Then it will append the message onto "stringer" using this line "stringer.append(sequenceNumber++ + ". " + message.substring(2) + "\n");", then lastly it will return the string onto the page using this line "return stringer.toString()"

![Image](Screenshot 2023-11-05 at 4.54.40 PM.png)
![Image](Screenshot 2023-11-05 at 4.54.44 PM.png)

It will use the same code to run this as well.

## Part 2
Using ls on the command lines
I tried to run ssh on my computer multiple times and it didn't work and I even changed the password but still nothing.

## Part 3
I've learned how to create a server and display what I would want using my code. I also learned how to correctly use some of my skills from my other courses and apply my learnings in this course. I also know how to work the terminal in a wider scale in order to locate files and make sure I know my location at all times.
