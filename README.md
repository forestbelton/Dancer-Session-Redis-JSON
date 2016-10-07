# NAME

Dancer::Session::Redis::JSON - Session store in Redis with JSON serialization

# VERSION

version 0.002

# SYNOPSIS

    session: "Redis::JSON"
    redis_server: "127.0.0.1:6379"

# DESCRIPTION

This module implements a session store on top of Redis. All data is
converted to JSON before being sent to Redis, which prevents invocations of
`Storable::nfreeze`. This common format allows the data to be shared among web
applications written in different languages.

If `redis_secret` is specified, all generated session IDs will be of the
form `id.base64_mac`. This is to maintain compatibility with the session store
mechanism that [Express](http://expressjs.com/) uses.

# NAME

Dancer::Session::Redis::JSON

# AUTHOR

Forest Belton <forest@homolo.gy>

# COPYRIGHT AND LICENSE

This software is Copyright (c) 2014 by Forest Belton.

This is free software, licensed under:

    The MIT (X11) License
