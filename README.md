## Table of Contents

- [Ideas-Features](#Ideas-Features)
- [MVP](#MVP)
- [Data Docs](#Data-Docs)
- [Tech Stack](https://github.com/MrNtlu/Project-Consumer/wiki/Tech-Stack)
  - [Android](https://github.com/MrNtlu/Project-Consumer/wiki/TS-Android)
  - [Backend](https://github.com/MrNtlu/Project-Consumer/wiki/TS-Backend-Database)
  - [Frontend](https://github.com/MrNtlu/Project-Consumer/wiki/TS-Frontend)
  - [Scraper](https://github.com/MrNtlu/Project-Consumer/wiki/TS-Scraper)
  - [iOS/Flutter](https://github.com/MrNtlu/Project-Consumer/wiki/TS-iOS-Flutter)
  - [Recommendation](https://github.com/MrNtlu/Project-Consumer/wiki/TS-Recommendation-System)
- [Mobile Design Ideas](https://github.com/MrNtlu/Project-Consumer/wiki/Design-Mobile)

# Decide
- Store Description
```
Introducing our fantastic new mobile application that's perfect for anyone who loves to keep track of the media they watch or play! With our app, you'll have access to an incredible array of Anime, Movies, TV Shows, and Games, all at your fingertips.

Our app makes it easy to discover new content that you're sure to love. With powerful search features, you can quickly find exactly what you're looking for. Once you've found your favorite content, you can add it to your list and give it a score, so you never forget which ones you enjoyed the most.

One of the best features of our app is the ability to create custom watch and play lists. Whether you're saving content to enjoy later or creating a playlist for a binge-watching session, our app makes it simple and convenient.

So what are you waiting for? Download our app today and start tracking, discovering, and enjoying all your favorite content like never before!
```

- Application Name
  * MyScreenList (MSL)
  * WatchPlayRepeat (WPR)
  * ScreenAndPlay (S&P)
  * WatchPlayRate (WPR)
  * MediaTrackr 
- Domain Name
- Logo
  * Canva
  * LogoMakr
  * Logojoy
  * Ucraft
  * Hatchful
- Color Palette

# TODO
- Add logs to backend for future leveling system
- TV Series rate each season not full tv series
- Get genres for Mobile
  * Anime
    * https://myanimelist.net/anime/genre/1/Action
    * https://api.jikan.moe/v4/genres/anime
  * Movie/TVSeries
    * Get image links with matching genres.
    * https://api.themoviedb.org/3/genre/movie/list?api_key=e3da88a1a7e7b8afd3a7d07638970529&language=en-US
    * https://api.themoviedb.org/3/genre/tv/list?api_key=e3da88a1a7e7b8afd3a7d07638970529&language=en-US
  * Game
    * https://api.rawg.io/api/genres?key=ca436d9694794822b768ab4f1490ebd5

# Ideas-Features

- **Email Suggestion System**
  * Send emails to users and let them opt-in out.

- **Logs/History**
  * Keep logs by date

- **User Interactions**
  * Rate content.
  * Add content as watching/watched/plan to/dropped.
  * Suggest similar content.
  * Create/Share custom list.
  * Suggest content
  * Suggest genre/tag from default genre/tags for content.
  * Add Friends
  * Show ratings and recommendations of friends.

- **Level System**
  * Users will level up depending on how much they've watched and rated.
  * After some time, leaderboard can be added.
  * User feedbacks will give points.
  * Their contribution via feedback systems and recommendations will be rewarded.
  * In the future, people who invite their friend will receive monthly premium if possible.
  * Survey system, ask users for their opinions favourites etc. and reward them.

- **What's Next**, recommendation based on user.
  * Allow users to give feedback, liked or remove.
  * Users should be able to opt-out or prefer genres.

- **Consume Later**, this feature will allow users to add content to consume next. Like listing movies to watch, games to play etc.

- **Legend Content**, these are content that you play/watch multiple times. After x time of watch/play they'll be marked as legend for that user.
  * Watched/Played x times.

- **Recommendation system**, based on content make recommendations.

- **Extra Content Attributes**
  * Available Platforms
  * If currently airing, reminders.
  * Upcoming series, reminder.


# Data Docs

- [Anime Docs](https://github.com/MrNtlu/Project-Consumer/wiki/API-Docs-Anime)
- [Games Docs](https://github.com/MrNtlu/Project-Consumer/wiki/API-Docs-Games)
- [Movie/TvSeries Docs](https://github.com/MrNtlu/Project-Consumer/wiki/API-Docs-Movie-TVSeries)
- [Others](https://github.com/MrNtlu/Project-Consumer/wiki/API-Docs-Others)




