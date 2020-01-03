# Introduction
This is the frontend of my final year project in school. I worked on a team with two other brillant course mates.
My job was to handle the IoT part of the project
- I wrote c code on the arduino for sending data online via a wifi module
- I built a simple website to display the data received and alert users on the site(that is the code on this repo)


## Basic flow
- Once the page is opened:
  - The data in the local storage, if any, is presented as a table.
  - Js code runs in the background to ocassionally poll data from thingspeak, the platform the arduino sends the data to.
- Once new data is received, it compares the data received with the data in the local storage of the browser:
  - If the data is the same no alert is shown.
  - If the data is different, the data is saved, then an alarm(a gong) is played, alerting the user of a change, the data is also flashed with red to serve as a virtual alert.
  - Polling continues.
  
### Notice
I built this project in less than two days(both the embeeded side and this site), so there are many things I looked over during implementation. For example:
- User management, this doesnot exist.
- Storage(the only storage used is the user's browser so the same user using different browsers will have different experiences).
