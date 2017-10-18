# FoodRader 🕵🏼‍♀️
Student name : WONG CHUN KIU

Student id : 14112109d

University: PolyU HK

# Index
<!-- TOC -->

- [FoodRader 🕵🏼‍♀️](#foodrader-🕵🏼‍♀️)
- [Index](#index)
- [Objective](#objective)
- [What](#what)
- [How](#how)
- [Why](#why)
- [Background](#background)
- [Project methodology](#project-methodology)
- [Resources estimation](#resources-estimation)
- [Design](#design)
    - [Dishes](#dishes)
    - [Drinks](#drinks)
- [Reference](#reference)
- [UML](#uml)
- [Database schema](#database-schema)
- [Required tech](#required-tech)
    - [Front end](#front-end)
    - [Backend](#backend)
    - [Database](#database)
    - [Image storeage](#image-storeage)
- [Required tools](#required-tools)
- [Appendix](#appendix)
- [Question ?](#question-)

<!-- /TOC -->

# Objective
Help foreigner to read the menu.

# What
Hong Kong is a international city. Residents in Hong Kong might not able to read  chinese. 

In order to have a lunch / dinner in local restaurant, they always need to carry a local person for menu translation. 

The goal of this application is to automatic that translation process and reduce the human resouces FoodRader will be a nice solution. 

The mission of FoodRader is help non-local person to place an order including read, pronounce and imagine the dish.

# How
In order to build a self service order placing application, crowdsource will become our standpoint. Every local restaurants will have some local customer, that we can collect an image, cantinese pronounce and GPS from those local customers as wall as the feedback with each dish. 

Mobile will be we primary platform to serve the customer.

Firebase will be a nice solution to store the data.

# Why
FoodRander enable those non-chinese customer to place an order via show the image, pronunciation and ranking based on their current GPS and localtime.

# Background
![Population Aged 5 and Over by Usual Language and Year](https://i.imgur.com/6Oe8YSh.png)
According to the report from the Hong Kong government that nearing 300,417 residents is majorly using english for their daily [1]. Those residents might not able to speack cantinese. However, they also needed to have lunch and dinner. 

![Population by Year, Usual Spoken Language and Whether Able to Speak Cantonese](https://i.imgur.com/VhXw4bp.png)
Inside that group, up to 220,000 people cannot specker cantinese. Therefore, it is a huge market for us to explore.

Once if we can active those person in Hong Kong that it will incream the income of the local restaurants.

# Project methodology
1. Collect the time slot of the user will have a lunch
    - Interview
1. Collect the food the daily menu of the target 
    - Onside
1. Collect the cantinese jyutping
    - Crowdsource
    - [Chinese Character Database](http://humanum.arts.cuhk.edu.hk/Lexis/lexi-can/)
    
# Resources estimation
- 2 weeks for study the front end framework
- 2 weeks about the use case study
- 1 week about system design
- 2 debuging of the product
-  1 week user accept test
- 1 week new feature based on accept test

# Design
## Dishes
![Design 1](https://i.imgur.com/bd5Kark.png)
## Drinks
![Design 2](https://i.imgur.com/jsWncQJ.png)
# Reference
1. [Population Aged 5 and Over by Usual Language and Year](http://www.bycensus2016.gov.hk/en/bc-mt.html)
1. [Population by Year, Usual Spoken Language and Whether Able to Speak Cantonese](http://www.bycensus2016.gov.hk/en/bc-mt.html)
1. [No hablar Cha Chaan Teng lingo](https://www.ovolohotels.com/cha-chaan-teng-lingo/)

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

