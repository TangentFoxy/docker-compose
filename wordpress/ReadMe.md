# Wordpress
This instance has a long history, as I've migrated my blog several times. As a
result of previously not keeping records, I've lost some of the history of how
it got here.

Ultimately, I had to modify the docker-compose I'd made for Pressbooks to make
this work (originally [from here](https://github.com/TangentFoxy/pressbooks-compatible-wordpress-dockerfile/blob/main/docker-compose.yml)).

I briefly tried [the version from awesome-docker-compose](https://github.com/docker/awesome-compose/blob/master/wordpress-mysql/compose.yaml),
but it doesn't support the ability to make basic edits to a Wordpress install,
yikes! (It also used a bad method for setting the database root password. D:)
