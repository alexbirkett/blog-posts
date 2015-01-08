#Javascript / CSS not gziped on wordpress site served by nginx

21, 2012

css, gzip, javascript, nginx

Having enabled gzip on my wordpress site, it took a while to figure out why css and javascript were still being served uncompressed. Well, the solution is here

You need to add

    gzip_types application/x-javascript text/css;

to the server block in your nginx config

