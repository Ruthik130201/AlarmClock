# CodeClause_AlarmClock
Modules Used: 
==> datetime
Python has a module named datetime to work with dates and times.
It provides a variety of classes for representing and manipulating dates and times, as well as for formatting and parsing dates and times in a variety of formats.
eg: import datetime

# get the current date and time
now = datetime.datetime.now()
print(now)  

Output: 2022-12-27 08:26:49.219717

Here, we have imported the datetime module using the import datetime statement.
One of the classes defined in the datetime module is the datetime class.
We then used the now() method to create a datetime object containing the current local date and time.

==> winsound
The winsound module in Python provides an interface to interact with the sound playing machinery in Windows. The PlaySound function plays or stops a given WAV sound file. The syntax of the PlaySound function is as follows:
winsound.PlaySound(sound, flags)
=>Parameters
sound is an object that specifies the sound that is to be played. The following table summarizes the built-in sounds in every Windows platform:
   sound string	           Corresponding control panel sound
 'SystemAsterisk'	                   Asterisk
 'SystemExclamation'               	Exclamation
 'SystemExit'	                      Exit Windows
 'SystemHand'	                      Critical stop
 'SystemQuestion'	                    Question

flags is a parameter that takes in winsound.SND_ flags. These flags provide additional commands to the play sound function. The following table summarizes the different flags and their usage:
    Flag	                                        Usage
winsound.SND_FILENAME	            Specifies that the sound parameter given is a WAV file name.
winsound.SND_ALIAS	              Specifies that the sound parameter given is a built-in sound. If the built-in sound does not exists, the default system sound is                                       played, unless winsound.SND_NODEFAULT is specified.
winsound.SND_LOOP             	  Specifies that the sound must be played repeatedly. This is a blocking call; in order to play the sound in a loop in the background,                                   winsound.SND.ASYNC must be specified.
winsound.SND_MEMORY	              Specifies that the sound is a byte-like object that contains data in WAV format. Using this flag together with winsound.SND_ASYNC                                       will raise a RuntimeError.
winsound.SND_PURGE	              Specifies that all instances of the given sound must be stopped. This flag is not supported on modern Windows platforms.
winsound.SND_ASYNC	              Specifies that the function should return immediately, allowing for the sound to play in the background.
winsound.SND_NODEFAULT	          Specifies that if the specified sound is not found, the system default sound must not be played.
winsound.SND_NOSTOP	              Specifies that sounds currently playing must not be interrupted.
winsound.SND_NOWAIT	              Specifies that the function must return if the sound driver is busy. This flag is not supported on modern Windows platforms.

Return value:: PlaySound returns None.
eg: import winsound
winsoud.PlaySound('SystemHand', winsound.SND_ALIAS)
winsoud.PlaySound('abcd', winsound.SND_ALIAS)
winsound.PlaySound('Fire_Alarm.WAV', winsound.SND_FILENAME)

Output: In the example above, in the first PlaySound function call, the Critical Stop built-in sound is played. In the second PlaySound function call, the default built-in sound is played, since abcd is not a built-in sound in Windows. The last PlaySound function call passes the name of the sound file as the sound argument. To specify that the passed sound argument is the name of a sound file, the winsound.SND_FILENAME flag is used. Therefore, if the Fire_Alarm.WAV file exists, it will be played; otherwise, a beep sound will be played.

==> mainloop
window.mainloop() tells Python to run the Tkinter event loop. This method listens for events, such as button clicks or keypresses, and blocks any code that comes after it from running until you close the window where you called the method.
