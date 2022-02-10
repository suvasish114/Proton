# Software Requirements Specification

Women’s safety is a big concern which has been the most important topic to date. Women’s safety matters a lot whether at home, outside the home, or working place. Few crimes against ladies particularly rape cases were terribly dread and fearful. Most of the women of various ages, till this day, are being subjected to violence, domestic abuse, and rape. As ladies ought to travel late at night generally, it’s necessary to remain alert and safe. Although the government is taking necessary measures for their safety, still, there are free safety apps for women that can help them to stay safe. Most females these days carry their smartphones with them, so it is necessary to have at least one of the personal safety apps installed. Such a security app for ladies will definitely facilitate in a way or the opposite. This is a user-friendly application that can be accessed by anyone who has installed it on their smartphone. Our intention is to provide you with the fastest and simplest way to contact your nearest help. In this system the user needs to feed some contact numbers, in case of an emergency on moving the phone up and down thrice, the system sends SMS and calls on one of the numbers fed into the system with the location.

## Purpose
Women's safety involves strategies, practices, and policies which aim to reduce gender-based violence (or violence against women), including women's fear of crime. Women's safety involves safe spaces. By making Women Safety Application we are giving a safe and secure society through digital ways. This document gives detailed functional and non-functional requirements for Women Safety Application – a full-featured application to provide women security. The purpose of this document is that the requirements mentioned in it should be utilized by software developers to implement the system.

## Scope of project
This software system will be an android based application, which allows users to download to use. This system is designed to make a quick response at the sender side and notify individuals when help is needed. This system allows people to send all necessary information including GPS location to authorized members whenever help is needed. With the help of this system, people should be able to call for help in an emergency from anywhere. 

## Category
This is mobile based application, that ensure user safety in a digital way.

## Product Prespective
This application will help any needy person in our society, especially women and girls. This application is based on live geo-location, for tracking the needy for help. This will help many customers if they once try to help us with some minute information. This application is based on self-governed issues and fully automatic once you get your work done. This can help a vast number of users subsequently all over the societies for their safety. This will ensure women's safety in every corner of our society and will help females to be calm & cool even in a critical situation. The context of the original product is specified in this SRS. For example, the user downloads the application and customizes some settings as needed, and adds some authorized contact numbers to notify when needed. By doing this, the user connects herself with the central database, which is hosted live. When the user presses the emergency alert button, the database starts sending notifications and live GPS locations at the authorized contact numbers. The diagram in the following figure presents the overall perspective of the development expected by the SRS. Here the sender side alert will be sent, and the alert will update the database, and immediately send custom notifications, with GPS longitude and latitude to the authorized contacts lists. Also, the user can change her notification type and custom the actions settings.

## Product features
This section summarizes the major features that the product contains or significant functions that let the user perform. The main goal of making this application is to make quick responses as needed. To achieve this goal, the app should be less complex, responsible, and fast. The app user interface is divided into two main subordinates. One for the user to send a response, and another is to receive the response. The user can custom all sending data types and messages and can set response methods as well. Users can also customize the response type as 5 times press the power button so that the user can make quick requests to the server. Also, the application can make auto voice calls to notify the authorized contact lists. 

## Assumptions and dependencies	
The application is fully free to use for everybody and it’s very handy to use anywhere anytime. For full-fledged services from us are some of your mobiles permissions such as:

- Your mobile should be connected with internet connectivity.
- Your mobile’s GPS location should be on.
- Your mobile should have a well-defined camera for auto capturing photos to give our services as soon as possible by identifying your location through A.I.
- You can directly connect to us by tapping your screen lock button 5 times.

## Users of System
Two types of users should be able to use this software. One user should be able to send an emergency notification to the mobile device of the other type of user, and the other type of user should be able to receive an alert about the situation of the previous user. The two types of users are,

- **Sender:** This is the user who is expecting some kind of assistance in case of an emergency.
- **Receiver:** These types of users are the users who are expected to provide the required assistance in case of an emergency.

## Functional Requirements
	
**Sender:**

- The sender should be able to create an account in the mobile application.
- The sender should be able to decide whom to send the notification to in case of an emergency.
- The sender should be able to choose among the various features of the application, whether to use that feature or not.
- The sender should be able to turn off the features of the mobile application.
- The emergency alert should be sent to the receiver whenever the sender shouts “Help” three times in a row.
- The emergency alert should be sent to the receiver wherever the sender presses the power button of her mobile device five times in a row.
- The sender’s alert should reach all the receivers.

**Receiver:**

- The receiver should be able to get the emergency notification properly whenever the sender is in an emergency situation.
- The receiver should get the proper location update of the sender.
- The receiver should get a live audio update of the sender’s situation if it is possible.
- The receiver should be notified whenever the alert reaches her device.

**Administrators:**

- The administrators should be able to view the requests sent from the sender’s device.
- The administrator should be able to interact with the database of the application.
- The administrators must be able to delete, update created accounts in the application.
- The administrator must be able to view a request log.
- Only the users with respective rights (administrators) should be able to use all the “Administrators” features.  

### Entity-relationship diagram

**Entity:**

- User(user_id, user_name, user_dob) User.user_id is the primary key.
- Location(location_id, longitude, latitude) Location.location_id is the primary key.
- Request(request_id, user_id, location_id, request_time) Request.request_id is the primary key.
- Response_info(info_id,request_id,camera_enable,audio_enable, call_enable, custom_message) Response_info.info_id is the primary key.
- Contact_list(contact_id,user_id,priority,mobile_numbers) Contact_list.contact_id is the primary key.

**Relationship:**

- User, location has 1:1 relation
- User, request has 1:1 relation
- Request, response_info has 1:n relation
- request , contact_list has 1:n relation

## Non-functional Requirements
As a mobile application, based on the “Android” operating system, the application would use a server. Whenever the sender sends a request, it will reach the receiver through the server. As an emergency application, we’ll have to make sure that the server of this system works in perfect condition 24*7, and because of the nature of the application, the application should have a response time, preferably less than 1 second. By any chance, if the response time exceeds, we need to make sure that the request from the sender reaches the receiver again.

## Interface Requirements
The user interface of this particular mobile application should be very easy to understand and use. We would preferably choose the GUI option to make the user interface of this application.

**Software Interface:**

- The software interfaces required for this application are,
- An internet connection.
- A central server.
- A mobile device with the Android operating system.

## Other Requirements:

**Security Requirements:**

The mobile application should be secured enough. It should be secured from all the hackers out there.

**Reliability:**

This system should be highly reliable and it should be able to transfer all the correct information in the correct order.

**Availability:**

Women safety applications are developed to assist whenever needed. This application is sensitive and needs to be active all the time. For this purpose, the system should be available 24*7 hours.

**Maintainability:**

The system should be maintainable in such a way that if any new requirement occurs then it should be easily implemented in the system.

**Reusability:**

This system provides emergency service. The system should work efficiently and fast. For this reason, the software should remain usable as long as people want to use this.

## References: 

- https://www.preventionweb.net/files/13380_7380832AssesmentFinal1.pdf
- https://u.search.msu.edu/?client=CSE&sitesearch=www.cse.msu.edu&analytics=UA-12345678-9&q=srs
- https://www.reqview.com/doc/iso-iec-ieee-29148-srs-example
