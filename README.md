# Park4night api

> Hello 👋🏽, below you will find the list of public park4night apis that I retrieved by monitoring the api calls of the IOS application. 📲<br />Although the api are public and are not protected by any kind of authentication, I believe that the creators of the park4night app do not want you to use them. 🤬

> These Apis rather make me realise how without a big refactor job the park4night app will continue to suck (despite there being thousands of great places). 🌄<br />I would like an app where I can filter places by most recent reviews, I can attach photos to my review or 'I'm here', each place is given a score based on reviews, number of people who have been there and lots of other things. </br>The idea of the app is good, but the implementation sucks. 💩 I have written several times to Frédéric, its creator, but although they are hiring, they don't take you full-remote (in 2023 🫢).

> I don't know the laws and regulations about this but every now and then I am tempted to scrap all their data and do an open-source project.💭💭

## General apis

- Get places from gps coordinates

  `https://guest.park4night.com/services/V4.1/lieuxGetFilter.php?latitude=<latitude>&longitude=<longitude>`

  Params

  - latitude (es 42.3383)
  - longitude (es 9.5367)

  Return a list of 200 [Place model](models/place.model.md).

- Get reviews from place id

  `https://guest.park4night.com/services/V4.1/commGet.php?lieu_id=<place_id>`

  Params

  - place_id (es 303989)

    Return a list of [Review model](models/review.model.md).

## User related apis

- Get places created by a user (from username)

  `https://guest.park4night.com/services/V4.1/lieuGetUser.php?uuid=<username>`

  Params

  - username (es gtosee)

  Return a list of [Place model](models/place.model.md).

- Get places reviewed by a user (from user id)

  `https://guest.park4night.com/services/V4.1/lieuGetCommUser.php?user_id=<user_id>`

  Params

  - user_id (es 372940)

  Return a list of [Place model](models/place.model.md).

- Get places visited by a user (from username)

  `https://guest.park4night.com/services/V4.1/lieuGetCommUser.php?user_id=<username>`

  Params

  - username (es gtosee)

  Return a list of [Place model](models/place.model.md).
