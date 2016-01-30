# ianblenke/coturn:latest

This is an autobuild docker image repo for an Alpine based 44M image build of coturn.

This builds from the origin source tree:

https://github.com/coturn/coturn

The startup script will auto-discover a public and private IP address, which can be 
environmentally overridden.

The startup script will also accept a `JSON_CONFIG` environment variable containing a
JSON formatted string with a `config` key array of lines to add to the generated 
coturn configuration file.

There is presently support compiled in for sqlite3, redis, mysql, and postgresql.

Note: Mongo support is commented out, as it adds 130M to the image size.

