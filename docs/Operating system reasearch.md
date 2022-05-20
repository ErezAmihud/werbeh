# Winapi and react os research
The next suspect is the oprating os itself.
Note that the more likely suspect is the text processing part of the application (unicode library), but then I would have proven it and ended the research early, meaning less fun for me.

## Windows locale
Windows locale is the way windows stores in what region your windows computer operates, what the calander you are using, the time format you are using (or the one you set for yourself), timezone and everything else.

My spider sense and my hope drove me to look into it and I found a few interesting things
- [LOCALE_IREADINGLAYOUT](https://docs.microsoft.com/en-us/windows/win32/intl/locale-ireadinglayout)
- [[set_layout_oriantation]] - that does not help, but is kinda nice

The [LOCALE_IREADINGLAYOUT](https://docs.microsoft.com/en-us/windows/win32/intl/locale-ireadinglayout) property is a string [[resource]] attached to a specific language (later in [[react os#React os|react os]] it will be explained better) in a compiled exe/dll that is meant (the best way to explain it is reading the react os source).

So I tried to find it online, and found nothing beside the windows documentation.
I noticed that the windows documentation stated that the functionality of translating a program/dll to different languages has moved to [[mui]] files, and indeed my windows 10 programs had mui files as resources.

After realising I can't use my computer to get or change this string without changing the mui file data.
To avoid interacting with multiple parsing issues and changing things in a compiled dll, I resorted to use [[react os#React os|react os]], which I can look at the source code that I want, yay.
