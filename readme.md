# [The Christchurch Ruby](https://christchurch.ruby.nz/) website!

This is designed to run on GitHub Pages, using Jekyll. It's a static site, so no
server-side processing is possible.

The guiding principle is *simplicity*. At time of writing, I have implemented:

- A home page with a brief description of the group and a list of all the meetups.
- A page for each meetup, with a description of the event.
- A [ICS feed] for scheduled meetups and future meetup dates.

Things I almost implemented but thought better of:

- A way to see future meetup dates
- An RSS feed for events.
- Event metadata like host, speaker, etc, including cute avatars from Gravatar or GitHub.
- A map of the meetup location.

[ICS feed]: https://github.com/berlinphp/berlinphp.github.com/blob/master/calendar.ics

## Adding a new meetup

To add a new meetup, create a new file in the `_events/{year}` directory. The filename should be the date of the event plus a description, in the format `YYYY-MM-DD-whatever.md`. Copy the most recent event file and update the details.

## Running locally

To run this site locally, you'll need to have Ruby installed. Then, run:

```
gem install jekyll
jekyll serve
```

There isn't a Gemfile, because it's really just emulating GitHub Pages and hoping for the best.
