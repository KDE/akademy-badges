# KDE Akademy Badge Generation

A collection of scripts that will generate a badge with a name and barcode, printed over the top of some additional information assets (for venue information, emergency information, schedule, etc). The barcode is simply an encoded user_id that we can scan to capture arrival time of attendees for both operational metrics (how many attendees are on site) and long-term planning metrics (how many attendees arrived against how many registered).

### Prerequisites

 * Ruby Bundler
 * Graphics (background1 for front page, background2 for back page)
 
To get up and running:

```bash
$ bundle install
$ ruby badge_from_cli.rb {userid} {name} {irc_nick}
```

### Generating from CSV, or API

To simplify automation, it is possible to generate a CSV file that we can loop through, the format of this CSV is as follows:

 * userid
 * name
 * ircnick

To use the API of the registration system, you will need to update the cookie value and the conference slug within the URL on lines 52 and 54 respectively. Ideally, we can migrate this to API keys, but there is no true need for this at the given time.
