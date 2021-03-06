osm_maps, OpenStreetMap Maps plugin
========

osm_maps plugin for osclass.org Open Source Classified

This plugin shows OpenStreetMap map for each item.

You should upgrade to the version 1.0.3. as Mapquest introduced a free API key starting from September 15, 2015.

Register and get your free API key at https://developer.mapquest.com/ . It takes a minute or so.Then add your API key in the file: \oc-content\plugins\osm_maps\index.php in this lne:

const MAPQUEST_API_KEY ='you_key_here';

it should look like this:

MAPQUEST_API_KEY ='Mf0UOnA76bfMm6Gzpqj8dFFBMGxP7KhY';

It requires activated:

allow_url_fopen = On

in the server php.ini file (requires server restart),

as it uses simplexml_load_file PHP function. It can be checked if it is activated via standard phpinfo(); call.

If it is not activated, and if you have no access to php.ini file on the server, try to put: 

php_value allow_url_fopen On 

into .htaccess file in the root folder of the server.

Google Maps plugin should be deactivated before installation.

If a house number is not mapped on the OpenStreetMap, one can add it on the map himself, as it is a wiki-style map (see www.osm.org for details).

The license of the OpenStreetMap allows to use it for free for commercial projects, even with high traffic volumes.

To install the plugin - put the two files index.php and map.php into the "osm_maps" folder and zip the folder with these two files into osm_maps.zip archive.

The plugin uses MapQuest Open nominatim free API. Please, read usage policy: http://developer.mapquest.com/web/products/open/nominatim
