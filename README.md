# iChat
# INFSCI 2560 Web Standard and Technology
Final Report

Hao Zhao(haz92),
Zhehao Lin(zhl140),
Zhehao Guo(zhg26)

## Introduction
Nowadays, people are increasingly using the social media to communicate with the world. The team decides to develop a social media website for our student to chat with friends, post texts, thumbs up and share images. 

## Objective
At first, we design the log in/ sign up functions for the website. People can sign up their own account with customized password longer that 5 digits. 
### Sign up
<img src="https://raw.githubusercontent.com/eherozhao/iChat/master/images/sign up.png" alt="sign up" align=center/>
Then they can log into the website and the website has cookies to store their login information. 

### Log in
<img src="https://raw.githubusercontent.com/eherozhao/iChat/master/images/log in.png" alt="log in" align=center/>

If the users enter the wrong password, the system will give them a notification with: Password is incorrect to let them input a new one.
<img src="https://raw.githubusercontent.com/eherozhao/iChat/master/images/login pass wrong.png" alt="wrong password" align=center/>

After succussfully entering in the main page, it has following functions for user to use:  seeing friends moment, posting texts and images, uploading profile, and following information.
### Main page
<img src="https://raw.githubusercontent.com/eherozhao/iChat/master/images/main page.png" alt="main page" align=center/>

The information about the users, the moments’ text and images are stored in the MongoDB with Atlas.
If people want to log out their accounts, they can directly click the “Logout” button and the page will jump back to the login page.
Next, the team implement all of the features in the main page. All of these functions are written by RESTful API and beyond the project assignment requirement, especially the real-time chat part.
### Moment
See others post and user's own post
<img src="https://raw.githubusercontent.com/eherozhao/iChat/master/images/moment.png" alt="moment" align=center/>
The frontend need to get the image and text information which has been posted into the database and then show them on the page.

### Text post
The users can text in the text field and click “POST”, then the text will be post into the moment part and also stored into the database.
### Image share
User should click “IMAGE” button first and then click “POST” to upload their images into the moment.
<img src="https://raw.githubusercontent.com/eherozhao/iChat/master/images/photo.png" alt="photo" align=center/>
Users have the privilege to upload the image they like to be their profile. This function will store the image information into the MongoDB database by using the Cloudinary API.
### Comment and thumbs up
<br>
<img src="https://raw.githubusercontent.com/eherozhao/iChat/master/images/add comment.png" alt="add comment" align=center/>
Users can comment others’ images and texts. Meanwhile, they can click the “thumbs up” button to demonstrate they like the post.


### Notification
<img src="https://raw.githubusercontent.com/eherozhao/iChat/master/images/notification.png" alt="notification" align=center/>
If users receive messages, the notification icon will have a red button to notify users that they have a message to read; in the same way, if someone follow the user, they will receive the notification. They can directly click “MARK ALL AS READ” to make all information as read.
<img src="https://raw.githubusercontent.com/eherozhao/iChat/master/images/notification follow.png" alt="notification follow" align=center/>

### Chat
This is the most important feature and the most difficult feature for the whole project. The team use Socket to implement the real-time chat systems.
<img src="https://raw.githubusercontent.com/eherozhao/iChat/master/images/chat.png" alt="chat" align=center/>

## Team Members' Contribution
Hao Zhao:
<br>
Angular JS: Login, Signup components(html + css + typescript)
<br>
Backend: Controller—login, signup, including token, hash code to
                password
<br>
Deploy Heroku
<br>
Making slide and report 
Zhehao Lin:
<br>
MongoDb design
<br>
Angular JS: auth-tabs, comments, followers and other components
<br>
Backend: Controller-function of sending friends, commenting, chatting etc. 
<br>
Server: socket for real-time chat
