# Jazz-Brite

**A jazz-themed web application inspired by Facebook Events.**

[See it live!](https://jazz-brite.herokuapp.com)

Today's jazz scene includes tons of exciting new artists, while numerous masters of the classic era continue to enrich and entertain. Jazz-Brite aims to provide a hub for sharing and exploring live happenings for what many call "America's premier art form".

<br />

![Jazz-Brite](app/assets/images/browsing_2.gif)

## Features

* Log in with Facebook credentials, or choose to create an account
* Create and edit events, and upload event pictures
* Send email invitations with a single click
* Receive email invitations and follow a link to RSVP
* Discover which events are happening near your browsing location
* View event locations and directions in Google Maps
* Request emails with a link for password reset

## Technologies

* Built atop Ruby on Rails, a PostgreSQL database, and the Heroku platform.
* Looks up event addresses and sets latitude and longitude via the Google Geocoding API.
* Locates users according to their IP address by using the IPinfo API, allowing the app to highlight upcoming events in the user's local area.
* Combines event and user location data through the Google Maps API, giving users an external link to view directions on Google's site.
* Enables users to login with their Facebook credentials by connecting to the Facebook OAuth API, so that users can skip creating a brand new account.
* Integrates Amazon Web Services (AWS) S3 Bucket to store uploaded images and serve them back to the application.
* Email invitations are delivered to inboxes with assistance from SendGrid.
* When users RSVP for events, dynamically modifies the layout via jQuery and AJAX.

## Local Environment Setup

1. Check that (a) Ruby, (b) Rails, and (c) Git are installed on your machine
2. Clone the repo: `$ git clone https://github.com/karafto/jazz-brite.git`
3. Move into the new directory: `$ cd jazz-brite`
4. Install gems: `$ bundle install`
5. Migrate the database: `$ rails db:migrate RAILS_ENV=test`
6. Run the test suite: `$ rails test`
7. Run the app: `$ rails server`

## Future Directions

* Commenting and liking on events
* For signed-up users, inviting via internal notifications
* Ability to make events private