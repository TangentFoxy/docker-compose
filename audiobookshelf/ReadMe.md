# Audiobookshelf
**WARNING**: Audiobookshelf takes an extremely long time to be ready for
connections, with no indication of when it will be ready. You will get
continuous 502 Bad Gateway errors until it resolves.

Modified from official instructions: https://www.audiobookshelf.org/docs/#docker-compose-install

**WARNING**: If you ever accidentally leave an old version of an Audiobookshelf
database where a new version can see it, a restart may cause it to load the old
database, and **its default behavior when this occurs is to delete every file it
doesn't recognize**. Thankfully, I had backups, but I have to set up all of the
metadata around this all over again now.

**WARNING**: Audiobookshelf doesn't clean up after itself, so when you modify
or remove items, it will bloat over time. I should replace it.

## Setup
During initial setup, you will be asked to create a library. I just call it
"Books", use `/audiobooks` for the path, and leave everything else at default.
