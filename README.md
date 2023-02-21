# Project Consumer

## Table of Contents
- [MVP](#MVP)
- [Websites for Data](#Websites-for-Data)
- [Ideas](#Ideas)
- [Tech Stack](#Tech-Stack)
- [Model Ideas](#Model-Ideas)
- [Android](#Android)
- [iOS](#iOS)
- [Scraper](#Scraper)
- [Backend](#Backend)
- [Database](#Database)
- [Frontend](#Frontend)
- [Recommendation](#Recommendation)

# MVP
Phase 1
- View/Search Movies etc.


Phase 2
- Scoring/Voting
- Mark as watched/planning/watching etc.

Phase 3
- Watch List (Watched/Plan to Watch/Dropped/Watching)

Phase 4
- Show recommendations
- Genre/Tag suggestions

Phase 5
- Create custom lists
- Share lists
- Add reviews

# Websites for Data
- https://www.themoviedb.org/
- https://www.igdb.com/api
- https://rawg.io/
- https://github.com/consumet/api.consumet.org
- https://api.thegamesdb.net / https://forums.thegamesdb.net/viewforum.php?f=10
- Extra Dataset's needed.

# Ideas
- Users can add/score etc.
- User's can create & share lists.
- Legend movies that you watch every x times.
- Legend movies and how many times watched.
- Upcoming series and notify.
- Currently airing and reminder.
- Available platorms
- Users should be able to make Genre/Tag suggestions from default genre/tags.
- App that will help you save clip or page of book/anime/movie/series
  E.g. input book/movie name, add tag, add category, 
- Recommendation system
  Based on movie, series and games make recommendations.

# Tech Stack
- Scraper [Reference](https://github.com/MrNtlu/Asset-Scraper)
- Backend [Not Decided]
- Database [MongoDB or PostgreSQL]
- Data/Data Analysis/AI for Recommendation [Not Decided]
- Frontend Web [Not Decided]
- Native Mobile

<sub>Check dribble for designs.</sup>

# Model Ideas

User
```
id
username
password
passwordResetToken
userType (Premium etc.)
createdAt
updatedAt
fcmToken
refreshToken
isMailNotificationAllowed
isAppNotificationAllowed
isOAuthUser
OAuthType
```

Content
```
id
title
description
imagePath
imdbID
language
type (Movie, Game, TV Series, Anime(if needed), etc.)
genreIds
externalScore 
externalScoreType (Metacritics/Imdb etc.)
score
scoreCount (How many voted)
listCount (How many people listed)
popularity (Should be calculated every week, score/scoreCount/listCount)
seasons (Custom model releaseDate, episodes, seasonNum. If movie or game episode and seasonNum is 1)
```

More...

# Android

Design Architecture: MVVM
Language: Kotlin
### Package Structure
```
├── model
│   ├── data
│   └── interfaces
├── adapters
├── service
│   ├── auth
│   └── main
├── di
├── repository
├── viewmodel
│   └── shared
├── utils
│   ├── Extensions.kt
│   ├── Utils.kt
│   ├── Constants.kt
│   └── Response.kt # Network Wrapper Class
└── ui
    ├── auth
    └── main
```

### Things to Search
- CI/CD (Github Actions CI, Firebase CD)
- Unit Test/Integration Test etc.
- Foldable Screens and Tablet support
- Deeplinking and Notification Redirection

### Rules
- Documentation in code.
- Naming rule for String, layout, file, function etc.

### Libraries
- savedStateHandle - Process Death Handling
- ViewBinding
- Onboarding library for introduction.
- Livedata, ViewModel, Coroutines and Flows.
- Okhttp - Interceptors and Authenticator. For JWT Login.
- Hilt - Dependency Injection
- Picasso or Glide - For image processing
- Retrofit, GSON - For API Requests
- Room - Caching
- DataStore - Local token, dark theme, authentication etc.
- Material 3/2 Depending on design needs.
- Shimmer - Loading effect.
- Lottie - Better animations.
- Leakcanary - Memory Leak detection.
- FCM - Firebase Cloud Messaging Notification.
- Firebase Crashlytics and Analytics
- RevenueCat or native in-app purchase.
- Jetpack Compose - For some UI implementations.
- Google Signin and/or Facebook Signin.
- Optional Libraries
    - CircleImageView, BlurImageView, Baseflow/PhotoView
    - zetbaitsu/Compressor.
    - ToggleButtonLayout
    - HideKeyboard
    - ShowcaseView
    - permissions-dispatcher/PermissionsDispatcher
    - FinestWebView-Android
    - fraggjkee/sms-confirmation-view, mukeshsolanki/android-otpview-pinview

# iOS

Design Architecture: MVC or MVVM (Needs Research)
Language: Swift

### Things to Search
- Caching
- Pagination

### Rules
- Documentation in code.
- Naming rule for String, layout, file, function etc.

### Libraries
- Firebase
- SwiftUI

# Scraper

### Deployment
- Github Actions (?)

### Libraries
- Cheerio
- Request-Promise
- Puppeteer
- Puppeteer-Extra 

# Backend

Language: JS, TS, Go (?)

### Things to Search
- Which stack to use
- Deployment options
- Elastic Search

# Database

MongoDB or PostgreSQL

### Things to Search
- Deployment options

# Frontend

Language: JS or TS

### Things to Search
- Which stack to use
- Deployment options

### Packages
- Tailwind Css

# Recommendation (Data/Data Analysis/AI)

Language: ?
Notes: Genre/tag should be the priority. Score should be taken into account but shouldn't effect that much.

