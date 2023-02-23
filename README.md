# Project Consumer

## Table of Contents

- [MVP](#MVP)
- [Websites for Data](#Websites-for-Data)
- [Ideas-Features](#Ideas-Features)
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

**Phase 1**
- View/Search Movies etc.
  - User login is not required but optional.

**Phase 2**
- Scoring/Voting
- Mark as watched/planning/watching etc.

**Phase 3**
- Watch List (Watched/Plan to Watch/Dropped/Watching)

**Phase 4**
- Show recommendations
- Genre/Tag suggestions

**Phase 5**
- Create custom lists
- Share lists
- Add reviews

# Websites for Data

Games (w/ Metacritic only)
- https://rawg.io/
- https://api.rawg.io/docs/#operation/games_list
- https://api.rawg.io/api/games?page=1&key=APIKEY&metacritic=1,100

Anime
- https://docs.api.jikan.moe/#tag/anime
- https://api.jikan.moe/v4/genres/anime

Movie/TVSeries
- https://www.themoviedb.org/
- https://developers.themoviedb.org/3/getting-started/introduction
- http://files.tmdb.org/p/exports/movie_ids_02_23_2022.json.gz
- http://files.tmdb.org/p/exports/tv_series_ids_02_23_2022.json.gz
- http://files.tmdb.org/p/exports/keyword_ids_02_22_2023.json.gz
- IMDB Flow -> https://api.themoviedb.org/3/movie/MOVIEID/external_ids?api_key=APIKEY > https://imdb-api.com/en/API/Title/APIKEY/IMDBID/Ratings

Others
- https://www.igdb.com/api
- https://github.com/consumet/api.consumet.org
- https://api.thegamesdb.net / https://forums.thegamesdb.net/viewforum.php?f=10
- https://myvideogamelist.com/
- Extra Dataset's needed.

# Ideas-Features

- **User Interactions**
  * Rate content.
  * Add content as watching/watched/plan to/dropped.
  * Suggest similar content.
  * Create/Share custom list.
  * Suggest content
  * Suggest genre/tag from default genre/tags for content.
- **What's Next**, recommendation based on user.
- **Consume Later**, this feature will allow users to add content to consume next. Like listing movies to watch, games to play etc.
- **Legend Content**, these are content that you play/watch multiple times. After x time of watch/play they'll be marked as legend for that user.
  * Watched/Played x times.
- **Recommendation system**, based on content make recommendations.
- **Extra Content Attributes**
  * Available Platforms
  * If currently airing, reminders.
  * Upcoming series, reminder.
- App that will help you save clip or page of book/anime/movie/series
  E.g. input book/movie name, add tag, add category, 


# Tech Stack

- Scraper [Reference](https://github.com/MrNtlu/Asset-Scraper)
- Backend (Django or MERN)
- Database PostgreSQL (Find Hosting)
- Data/Data Analysis/AI for Recommendation [Not Decided]
- Frontend Web [Not Decided]
- Android Native - Flutter iOS

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

Content (Anime - TVSeries/Movie - Games)
```
id
title
description
imagePath
imdbID
language
type (Movie, Game, TV Series, Anime(if needed), etc.)
genreIds (list)
tags (until decided how it should be handled automatically, should be internal use only.)
externalScore 
externalScoreType (Metacritics/Imdb etc.)
seasons (Custom model releaseDate, episodes, seasonNum. If movie or game episode and seasonNum is 1)
rate [CALCULATED]
rateCount (How many voted) [CALCULATED]
listCount (How many people listed) [CALCULATED]
popularity (Should be calculated every week, score/scoreCount/listCount or aggregated) [CALCULATED]
```

Status Enum
```
Active 0 (Watching/Playing)
Finished 1
Dropped 2
```

GameList
```
id
userID
gameID
rate
timesFinished
status (StatusEnum)
achievementStatus (% of game finished nullable)
```

MovieWatchList
```
id
userID
movieID
rate
timesFinished
status (StatusEnum)
```

TVSeriesWatchList
```
id
userID
movieID
rate
timesFinished
status (StatusEnum)
watchedEpisodes
```

ConsumeLater
```
id
userID
contentID
order (Consume order)
note (Nullable, note that user can leave for themselves.)
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

