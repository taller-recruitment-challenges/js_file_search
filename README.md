# js_file_search

Imagine that you have a very long list of file paths (path_list)
and that it is updated once a day.

You need to do a function to search for the existence of files in it
or folders. This function is going to be executed thousands of times per minute so
you must implement a resilient algorithm to the challenge situation

Tips:
- You cannot use regex
- All entries in path_list will start with " / "
- A wildcard may be present for the items to be searched " * "

```js
const path_list = [
    "/usr/bin",
    "/var/cache/apache2/mod_cache_disk",
    "/usr/bin/wget",
    "/var/cache/apache2",
];

const search_items = [
    "/usr/bin", // true
    "/usr/var", // false
    "/var/cache/*/mod_cache_disk", //true
    "/*/*/wget", //true
    "/var/cache/nginx"//false

];

```
