# Hello World.

This is how we make the CSZSA website. It uses Hugo and Forestry.io for the backend. We deploy using CircleCI to AWS. The site is static, but automatically deploys when we commit to Production.

## Forestry

Our backend CMS is Forestry.io. It allows us to manage the website and content without needing to edit source documents. Any changes made via Forestry are on our "Staging" server, so they will not automatically go to cszsa.com. The web manager will make any updates to the production site, including pushing changes from Staging into Production.

Within Forestry, content is broken into 3 different areas:

* Content
  - Blog
  - Epecial Events
  - Pages
    - Classes
    - Private Shows
    - etc
* Players
  - Player Data (nickname, bio, etc)
  - Player Pages (display of above data, along with next shows, etc)
* Matches
  - Upcoming Matches
  - Match Recaps


## Match Schedules

We update the match schedule each month, and then cycle completed matches to the Match Recaps section. A match consists of metadata or "front matter," and a small section for content – ie the BYOB policy.

When Hugo renders the site, the front matter into the format for the match, including players and their photos, etc.

Additionally, we update the player page each month to include each players matches for that month. That gets rendered as a list of matches and ticket links.

Finally, after a match, we move the completed match to the "Match Recaps" section, and add the final scores, games played, and any fouls committed.  
