# 1. FoodRader 🕵
Student name : WONG CHUN KIU

Student id : 14112109d

University: PolyU HK

# 2. Index
<!-- TOC -->

- [1. FoodRader 🕵](#1-foodrader-🕵)
- [2. Index](#2-index)
- [3. Objective](#3-objective)
- [4. What](#4-what)
- [5. How](#5-how)
- [6. Why](#6-why)
- [7. Background](#7-background)
- [8. Project methodology](#8-project-methodology)
- [9. Resources estimation](#9-resources-estimation)
- [10. Design](#10-design)
    - [10.1. Dishes](#101-dishes)
    - [10.2. Drinks](#102-drinks)
- [11. Reference](#11-reference)
- [12. UML](#12-uml)
- [13. Database schema](#13-database-schema)
- [14. Required tech](#14-required-tech)
    - [14.1. Front end](#141-front-end)
    - [14.2. Backend](#142-backend)
    - [14.3. Database](#143-database)
    - [14.4. Image storeage](#144-image-storeage)
- [15. Required tools](#15-required-tools)
- [16. System architecture](#16-system-architecture)
- [17. Appendix](#17-appendix)
- [18. Question ?](#18-question-)

<!-- /TOC -->

# 3. Objective
Help foreigner to read the menu.

# 4. What
Hong Kong is a international city. Residents in Hong Kong might not able to read  chinese. 

In order to have a lunch / dinner in local restaurant, they always need to carry a local person for menu translation. 

The goal of this application is to automatic that translation process and reduce the human resouces FoodRader will be a nice solution. 

The mission of FoodRader is help non-local person to place an order including read, pronounce and imagine the dish.

# 5. How
In order to build a self service order placing application, crowdsource will become our standpoint. Every local restaurants will have some local customer, that we can collect an image, cantinese pronounce and GPS from those local customers as wall as the feedback with each dish. 

Mobile will be we primary platform to serve the customer.

Firebase will be a nice solution to store the data.

# 6. Why
FoodRander enable those non-chinese customer to place an order via show the image, pronunciation and ranking based on their current GPS and localtime.

# 7. Background
![Population Aged 5 and Over by Usual Language and Year](https://i.imgur.com/6Oe8YSh.png)
According to the report from the Hong Kong government that nearing 300,417 residents is majorly using english for their daily [1]. Those residents might not able to speack cantinese. However, they also needed to have lunch and dinner. 

![Population by Year, Usual Spoken Language and Whether Able to Speak Cantonese](https://i.imgur.com/VhXw4bp.png)
Inside that group, up to 220,000 people cannot specker cantinese. Therefore, it is a huge market for us to explore.

Once if we can active those person in Hong Kong that it will incream the income of the local restaurants.

# 8. Project methodology
1. Collect the time slot of the user will have a lunch
    - Interview
1. Collect the food the daily menu of the target 
    - Onside
1. Collect the cantinese jyutping
    - Crowdsource
    - [Chinese Character Database](http://humanum.arts.cuhk.edu.hk/Lexis/lexi-can/)
    
# 9. Resources estimation
- 2 weeks for study the front end framework
- 2 weeks about the use case study
- 1 week about system design
- 2 debuging of the product
-  1 week user accept test
- 1 week new feature based on accept test

# 10. Design
## 10.1. Dishes
![Design 1](https://i.imgur.com/bd5Kark.png)
## 10.2. Drinks
![Design 2](https://i.imgur.com/jsWncQJ.png)
# 11. Reference
1. [Population Aged 5 and Over by Usual Language and Year](http://www.bycensus2016.gov.hk/en/bc-mt.html)
1. [Population by Year, Usual Spoken Language and Whether Able to Speak Cantonese](http://www.bycensus2016.gov.hk/en/bc-mt.html)
1. [No hablar Cha Chaan Teng lingo](https://www.ovolohotels.com/cha-chaan-teng-lingo/)

# 12. UML
Use case diagram

![Use case diagram](https://i.imgur.com/RZZYK5e.png)

# 13. Database schema
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

# 14. Required tech
## 14.1. Front end
[Polymer](https://www.polymer-project.org/about)

## 14.2. Backend
[Firebase](https://firebase.google.com/products/)

## 14.3. Database
Type: NoSQL

[Cloud Firestore](https://firebase.google.com/products/firestore/)

## 14.4. Image storeage
[Cloud Storage](https://firebase.google.com/products/storage/)

# 15. Required tools
[Draw use case diagram](https://yuml.me/diagram/usecase/draw)

# 16. System architecture
![System architecture](https://i.imgur.com/6N55F7A.png)

# 17. Appendix
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

# 18. Question ?
Please report to alpha.wong@tuta.io

