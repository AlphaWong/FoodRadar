# FoodRader 🕵
Student name : WONG CHUN KIU

Student id : 14112109d

University: The Hong Kong Polytechnic University

Program: 61425 / BA(Hons) in Computing

Supervisor: Prof. YOU Jia Jane

# Index

# Assumption
Targeted user should be an english speaker.

# Objective
Help foreigner to read the menu.

# Acknowledgments
In order to initialize our current data set, [Milan Rajbhandari](gnumilanix@gmail.com) contributes a lot of photo about the dish as well as the menu. It offers the basic data set for the project database. Also, thanks the employee in Lalamove help me to test the idea. Meanwhile, Progressive web application will be adopted to FoodRader as it enable developer create a mobile friendly, low network consumption and Google chrome native support ( Both android and desktop ) application. Also, It should able to breakdown the current language issue between when non-cantonese person to place a order in Hong Kong. 

# Abstract
FoodFader aims to help the foreigner to place order in cantonese 

# What
Hong Kong is an international city. Residents in Hong Kong might not be able to read chinese. 

In order to have a lunch / dinner in local restaurant, they always need a local person for menu translating. 

The goal of this application is to automate that translation process and reduce the human resources. 

The mission of FoodRader would like to help non-local person to place an order including read, pronounce and imagine the dish.

# How
In order to build a self service order placing application, crowd sourcing will become our standpoint. As many of educated local people able to understand the context of menu in local restaurant. Also, selfie seems become a local well known culture that they willing to post their photo to share network that we just need to offer a share button which will draw their attention.

Meaning we can collect an image, cantonese pronounce and GPS from those customers as wall as the feedback with each dish. 

Mobile will be our primary platform to serve those customers.

Firebase will be a nice solution to store the data.

# Why
FoodRander enables those non-chinese customer to place an order via show the image, pronunciation and ranking based on their current GPS and local time.

# Background
![Population Aged 5 and Over by Usual Language and Year](https://i.imgur.com/6Oe8YSh.png)
According to the report from the Hong Kong government that nearing 300,417 residents is majorly using english for their daily [1]. Those residents might not able to speak cantonese. However, they also needed to have lunch and dinner. 

## Related Works
### Google map local guide program
[Google map](https://maps.google.com/localguides/rules) current starts a local guide program which will based on the mobile user daily location to pop-up a location related question for instance if you locate at PolyU daily, following questions might be pop-up in your mobile "Do PolyU have canteen ?", "Do PolyU is education related?" or "Do PolyU open to public enter ?".
![Google map local guide screen shot](https://i.imgur.com/EJCn3Sa.png)

### openrice.com
[openrice](https://i.imgur.com/OMKvc6F.png) enable customer to post review, photo and menu. It allows customer to many media related to subject restaurant. For instance, customer able to submit a dish photo which help customers expectation modeling. However, it is not mobile web browser friendly that the website in mobile is almost read only.

![openrice.com screen shot](https://i.imgur.com/OMKvc6F.png)

![Population by Year, Usual Spoken Language and Whether Able to Speak Cantonese](https://i.imgur.com/VhXw4bp.png)
Inside that group, up to 220,000 people cannot speck cantonese. Therefore, it is a huge market for us to explore.

Once if we can active those person in Hong Kong that it will incream the income of the local restaurants.

# Project methodology
1. Collect the time slot when the user will have a lunch
    - Interview
    - Start with my workmate ( native english speaker )
1. Collect the food the daily menu of the target 
    - Onside
1. Collect the cantonese jyutping
    - Crowd sourcing
    - [Chinese Character Database](http://humanum.arts.cuhk.edu.hk/Lexis/lexi-can/)
1. [Google Polymer](https://www.polymer-project.org/about) 
    - Web framework for progressive web application [PWA](https://developers.google.com/web/progressive-web-apps/)
1. [Firebase](https://firebase.google.com/)
    - Serverless service for project hosting.
1. [Google Analytics](https://www.google.com/analytics/#?modal_active=none)
    - Track the user activity in FoodRader.
    
# Resources estimation
- 2 weeks for study the front end framework
- 2 weeks about the use case study
- 1 week about system design
- 2 debug of the product
-  1 week user accept test
- 1 week new feature based on accept test

# Design
## Dishes
![Design 1](https://i.imgur.com/bd5Kark.png)
## Drinks
![Design 2](https://i.imgur.com/jsWncQJ.png)

# UML
Use case diagram

![Use case diagram](https://i.imgur.com/RZZYK5e.png)

# Database schema
```json
{
    "_id": "xxxxx",
    "userId": "xxxxx",
    "star": [
        {
            "userId": "userId0",
            "timeStamp": "9999999999",
        },
        {
            "userId": "userId1",
            "timeStamp": "9999999999",
        }
    ],
    "description": "xxxxxx",
    "thumbnail": [
        "thumbnailURI0",
        "thumbnailURI1",
        "thumbnailURI2",
    ],
    "gps": {
        "lat": "99.99",
        "long": "99.99",
    },
    "english": "rice",
    "jyutping": "faan",
    "cantonese": "飯",
    "type": "dish",
}
```

# Required tech
## Front end
[Polymer](https://www.polymer-project.org/about)

## Backend
[Firebase](https://firebase.google.com/products/)

## Database
Type: NoSQL

[Cloud Firestore](https://firebase.google.com/products/firestore/)

## Image storeage
[Cloud Storage](https://firebase.google.com/products/storage/)

# Required tools
[Draw use case diagram](https://yuml.me/diagram/usecase/draw)

# System architecture
![System architecture](https://i.imgur.com/6N55F7A.png)

# Progress
1. Initial database design
1. Initial UI design
1. Study the compatibility of mobile support
1. Study web analytics service
1. Study firebase deployment

# 16 Reference
1. [Population Aged 5 and Over by Usual Language and Year](http://www.bycensus2016.gov.hk/en/bc-mt.html)
1. [Population by Year, Usual Spoken Language and Whether Able to Speak Cantonese](http://www.bycensus2016.gov.hk/en/bc-mt.html)
1. [No hablar Cha Chaan Teng lingo](https://www.ovolohotels.com/cha-chaan-teng-lingo/)
1. [Building Progressive Web Apps](https://www.safaribooksonline.com/library/view/building-progressive-web/9781491961643/) ISBN-13: 978-1491961650 
# Appendix
```
// Use case diagram
[Customer]-(Sign In)
[Customer]-(Upload a dish)
(Upload a dish)<(Upload a timestamp)
(Upload a dish)<(Upload GPS)
(Upload a dish)<(Add star)
(Upload a dish)<(Upload image)
[Customer]-(Star a dish)
[Customer]-(Play a voice record)
```

# Question ?
Please report to alpha.wong@tuta.io
