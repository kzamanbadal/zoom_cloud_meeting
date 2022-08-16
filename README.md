Zoom Cloud Meeting Automation
A yii2 script that automatically joins a zoom meeting based on your timetable/schedule.

What does it do?
It performs the following processes:

Checks the "meetingschedule.csv" file to look for meetings that are going to start.
Checks the path of zoom application from path.txt to launch the app.
As soon as the current time matches any meeting time it opens the Zoom Desktop application.
Navigates the cursor automatically to various steps to join the meeting.
The meeting ID and passcode are extracted from "meetingschedule.csv" and entered into the Zoom app automatically.
Prerequisites
Zoom app must be installed in your system.
You must be logged in to your Zoom account.
Install Visual C++ Redistributable form net or file attached with it.
Meeting time for the day along with Meeting ID and passcode must be entered manually into the "meetingschedule.csv"
How to use with Python?
The best way to use my script is to firstly clone the git repo where you want to.
Be sure to add the location where Zoom.exe is installed in your system in the line 20 of the Code file.
Open "meetingschedule.csv" and fill in the Meeting Time, Meeting ID and Passcode of each meeting you want to join automatically.
Open "Zoom.py".
NOTE: Meeting Time must be in Hours and Minutes format only!

What happens behind the scene?
An infinite loop keeps checking the current time of the system using "datetime.now" funtion.
The zoom app is opened using "subprocess.Popen()" funtion as soon as current time matches the time mentioned in "meetingschedule.csv".
"pyautogui.locateOnScreen()" function locates the image of join button on the screen and returns the position.
"pyautogui.moveTo()" moves the cursor to that location.
"pyautogui.click()" performs a click operation.
The meeting Id and Passcode are entered using the "keyboard.write()" command.
