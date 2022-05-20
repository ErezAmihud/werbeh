### Black Box Research
At first I wanted to understand where the reversing is implemented, is it from the text processing application, the windows operating system or the app creator itself.


##### Message box 
I started with a simple message box to print 
I started creating a basic message box with a message, and trying to print english and hebrew letters.

As we expected, when giving the characters in english they were printed as left to right, and hebrew from right to left.
eg. when writing the english word {'h', 'e', 'l', 'l', 'o'} we would use {'ם', 'ו', ,ל', 'ש'} array.

Meaning there is nothing in the application itself (or data) to point to the fact that the text is reversed.


So we cross it from the list of suspects
- [x] The application
- [ ] The windows operating system
- [ ] Text processing application