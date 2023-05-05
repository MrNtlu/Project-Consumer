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
- Application Name (Pixel, Entertainment, Consume)
  * Consumeplay
  * EntertaiNation
  * Entertainz
  * Consumaplex
  * Enterticio
  * WatchPlayRate: This name highlights the core features of your app - users can watch or play content, and rate it.
  * MyScreenList: This name combines the idea of a personalized list with the screen-based entertainment your app provides.
  * FlickGameShow: This name plays on the idea of "flicking" through content, while also incorporating the different types of media your app covers.
  * EntertainMe: This name is simple and catchy, and suggests that the app is a one-stop-shop for all things entertainment.
BingeBox: This name conveys the idea of a container or repository for watching multiple episodes or seasons of a show in one sitting.
  * Watchlistify: This name combines "watchlist" (the feature in your app that allows users to add content they want to watch) with "ify" (a popular suffix used in tech company names).
  * ScreenVault: This name plays on the idea of a secure place to store all your favorite movies, TV shows, and games.

- Domain Name
- Logo
  * Canva
  * LogoMakr
  * Logojoy
  * Ucraft
  * Hatchful
- Color Palette

# TODO
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

- **User Interactions**
  * Rate content.
  * Add content as watching/watched/plan to/dropped.
  * Suggest similar content.
  * Create/Share custom list.
  * Suggest content
  * Suggest genre/tag from default genre/tags for content.
  * Add Friends
  * Show ratings and recommendations of friends.

- **Logs/History**
  * Keep logs by date

- **Level System** (Optional)
  * Users will level up depending on how much they've watched and rated.
  * After some time, leaderboard can be added.
  * User feedbacks will give points.
  * Their contribution via feedback systems and recommendations will be rewarded.
  * In the future, people who invite their friend will receive monthly premium if possible.

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

- App that will help you save clip or page of book/anime/movie/series
  E.g. input book/movie name, add tag, add category.

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

# Data Docs

- [Anime Docs](https://github.com/MrNtlu/Project-Consumer/wiki/API-Docs-Anime)
- [Games Docs](https://github.com/MrNtlu/Project-Consumer/wiki/API-Docs-Games)
- [Movie/TvSeries Docs](https://github.com/MrNtlu/Project-Consumer/wiki/API-Docs-Movie-TVSeries)
- [Others](https://github.com/MrNtlu/Project-Consumer/wiki/API-Docs-Others)




