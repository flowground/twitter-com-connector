# ![LOGO](logo.png) Twitter **flow**ground Connector

## Description

A generated **flow**ground connector for the Twitter API (version 1.1).

Generated from: https://api.apis.guru/v2/specs/twitter.com/1.1/swagger.json<br/>
Generated at: 2019-06-06T16:13:16+03:00

## API Description



## Authorization

This API does not require authorization.

## Actions

### Returns settings (including<br/>
> current trend, geo and sleep time information) for the authenticating user.

#### Input Parameters
* `trend_location_woeid` - _optional_ - The Yahoo! Where On Earth ID to use as the user's default trend location. Global information is
available by using 1 as the WOEID. The woeid must be one of the locations returned by GET
trends/available.

Example Values: 1
* `sleep_time_enabled` - _optional_ - When set to true, t or 1, will enable sleep time for the user. Sleep time is the time when push or
SMS notifications should not be sent to the user.

Example Values: true
* `start_sleep_time` - _optional_ - The hour that sleep time should begin if it is enabled. The value for this parameter should be
provided in ISO8601 format (i.e. 00-23). The time is considered to be in the same timezone as the
user's time_zone setting.

Example Values: 13
* `end_sleep_time` - _optional_ - The hour that sleep time should end if it is enabled. The value for this parameter should be
provided in ISO8601 format (i.e. 00-23). The time is considered to be in the same timezone as the
user's time_zone setting.

Example Values: 13
* `time_zone` - _optional_ - The timezone dates and times should be displayed in for the user. The timezone must be one of the
Rails TimeZone names.

Example Values: Europe/Copenhagen, Pacific/Tongatapu
* `lang` - _optional_ - The language which Twitter should render in for this user. The language must be specified by the
appropriate two letter ISO 639-1 representation. Currently supported languages are provided by GET
help/languages.

Example Values: it, en, es

### Updates the<br/>
> authenticating user's settings.

#### Input Parameters
* `trend_location_woeid` - _optional_ - The Yahoo! Where On Earth ID to use as the user's default trend location. Global information is
available by using 1 as the WOEID. The woeid must be one of the locations returned by GET
trends/available.

Example Values: 1
* `sleep_time_enabled` - _optional_ - When set to true, t or 1, will enable sleep time for the user. Sleep time is the time when push or
SMS notifications should not be sent to the user.

Example Values: true
* `start_sleep_time` - _optional_ - The hour that sleep time should begin if it is enabled. The value for this parameter should be
provided in ISO8601 format (i.e. 00-23). The time is considered to be in the same timezone as the
user's time_zone setting.

Example Values: 13
* `end_sleep_time` - _optional_ - The hour that sleep time should end if it is enabled. The value for this parameter should be
provided in ISO8601 format (i.e. 00-23). The time is considered to be in the same timezone as the
user's time_zone setting.

Example Values: 13
* `time_zone` - _optional_ - The timezone dates and times should be displayed in for the user. The timezone must be one of the
Rails TimeZone names.

Example Values: Europe/Copenhagen, Pacific/Tongatapu
* `lang` - _optional_ - The language which Twitter should render in for this user. The language must be specified by the
appropriate two letter ISO 639-1 representation. Currently supported languages are provided by GET
help/languages.

Example Values: it, en, es

### Sets which<br/>
> device Twitter delivers updates to for the authenticating user. Sending none as the device parameter<br/>
> will disable SMS updates.

#### Input Parameters
* `device` - _required_ - Must be one of: sms, none.

Example Values: sms
* `include_entities` - _optional_ - When set to either true, t or 1, each tweet will include a node called "entities,". This node
offers a variety of metadata about the tweet in a discreet structure, including: user_mentions,
urls, and hashtags. While entities are opt-in on timelines at present, they will be made a default
component of output in the future. See Tweet Entities for more detail on entities.

Example Values: true

### Sets values that<br/>
> users are able to set under the Account tab of their settings page. Only the parameters specified<br/>
> will be updated.

#### Input Parameters
* `name` - _optional_ - Full name associated with the profile. Maximum of 20 characters.

Example Values: Marcel Molina
* `url` - _optional_ - URL associated with the profile. Will be prepended with "http://" if not present. Maximum of 100
characters.

Example Values: http://project.ioni.st
* `location` - _optional_ - The city or country describing where the user of the account is located. The contents are not
normalized or geocoded in any way. Maximum of 30 characters.

Example Values: San Francisco, CA
* `description` - _optional_ - A description of the user owning the account. Maximum of 160 characters.

Example Values: Flipped my wig at age 22 and it never grew back. Also: I work at Twitter.
* `include_entities` - _optional_ - The entities node will not be included when set to false.

Example Values: false
* `skip_status` - _optional_ - When set to either true, t or 1 statuses will not be included in the returned user objects.

### Updates the authenticating user's profile background image. This method can also be used to enable<br/>
> or disable the profile background image. Although each parameter is marked as optional, at least one<br/>
> of image, tile or use must be provided when making this request.

#### Input Parameters
* `Content-Type` - _required_ - Content type header
* `tile` - _optional_ - Whether or not to tile the background image. If set to true, t or 1 the background image will
be displayed tiled. The image will not be tiled otherwise.
* `use` - _optional_ - Determines whether to display the profile background image or not. When set to true, t or 1 the
background image will be displayed if an image is being uploaded with the request, or has been
uploaded previously. An error will be returned if you try to use a background image when one is
not being uploaded or does not exist. If this parameter is defined but set to anything other
than true, t or 1, the background image will stop being used.
* `include_entities` - _optional_ - The entities node will not be included when set to false.

Example Values: false
* `skip_status` - _optional_ - When set to either true, t or 1 statuses will not be included in the returned user objects.

### Sets one or<br/>
> more hex values that control the color scheme of the authenticating user's profile page on<br/>
> twitter.com.<br/>
> Each parameter's value must be a valid hexidecimal value, and may be either three or six characters<br/>
> (ex: #fff or #ffffff).

#### Input Parameters
* `profile_background_color` - _optional_ - Profile background color. Example Values: 3D3D3D
* `profile_link_color` - _optional_ - Profile link color.Example Values: 0000FF
* `profile_sidebar_border_color` - _optional_ - Profile sidebar's border color. Example Values: 0F0F0F
* `profile_sidebar_fill_color` - _optional_ - Profile sidebar's background color. Example Values: 00FF00
* `profile_text_color` - _optional_ - Profile text color. Example Values: 000000
* `include_entities` - _optional_ - The entities node will not be included when set to false. Example Values: false
* `skip_status` - _optional_ - When set to either true, t or 1 statuses will not be included in the returned user objects.

### Updates the<br/>
> authenticating user's profile image. Note that this method expects raw multipart data, not a URL to<br/>
> an image. This method asynchronously processes the uploaded file before updating the user's profile<br/>
> image URL. You can either update your local cache the next time you request the user's information,<br/>
> or, at least 5 seconds after uploading the image, ask for the updated URL using GET<br/>
> users/profile_image/:screen_name<br/>
> (https://dev.twitter.com/docs/api/1/get/users/profile_image/:screen_name).

#### Input Parameters
* `Content-Type` - _required_ - Content type header
* `skip_status` - _optional_ - When set to either true, t or 1 statuses will not be included in the returned user objects.

### Returns the<br/>
> current rate limits for<br/>
> methods belonging to the specified resource families.<br/>
> <br/>
> Each 1.1 API resource belongs to a "resource family" which is indicated in its method documentation.<br/>
> You can typically determine a method's resource family from the first component of the path after<br/>
> the resource version.<br/>
> <br/>
> This method responds with a map of methods belonging to the families specified by the resources<br/>
> parameter, the current remaining uses for each of those resources within the current rate limiting<br/>
> window, and its expiration time in epoch time. It also includes a rate_limit_context field that<br/>
> indicates the current access token context.<br/>
> <br/>
> You may also issue requests to this method without any parameters to receive a map of all rate<br/>
> limited GET methods. If your application only uses a few of methods, please explicitly provide a<br/>
> resources parameter with the specified resource families you work with.

#### Input Parameters
* `resources` - _optional_ - A comma-separated list of resource families you want to know the current rate limit disposition
for. For best performance, only specify the resource families pertinent to your application.Example
Values: statuses,friends,trends,help

### Blocks the specified user from<br/>
> following the authenticating user. In addition the blocked user will not show in the authenticating<br/>
> users mentions or timeline (unless retweeted by another user). If a follow or friend relationship<br/>
> exists it is destroyed.

#### Input Parameters
* `include_entities` - _optional_ - The entities node will not be included when set to false.

Example Values: false
* `skip_status` - _optional_ - When set to either true, t or 1 statuses will not be included in the returned user objects.

### Un-blocks the user specified<br/>
> in the ID parameter for the authenticating user. Returns the un-blocked user in the requested format<br/>
> when successful. If relationships existed before the block was instated, they will not be restored.

#### Input Parameters
* `include_entities` - _optional_ - The entities node will not be included when set to false.

Example Values: false
* `skip_status` - _optional_ - When set to either true, t or 1 statuses will not be included in the returned user objects.

### Returns an array of numeric user<br/>
> ids the authenticating user is blocking.

#### Input Parameters
* `stringify_ids` - _optional_ - Many programming environments will not consume our ids due to their size. Provide this option to
have ids returned as strings instead. Read more about Twitter IDs, JSON and Snowflake.

Example Values: true
* `cursor` - _optional_ - Causes the list of blocked users to be broken into pages of no more than 5000 IDs at a time. The
number of IDs returned is not guaranteed to be 5000 as suspended users are filtered out after
connections are queried. If no cursor is provided, a value of -1 will be assumed, which is the first
"page."

The response from the API will include a previous_cursor and next_cursor to allow paging back and
forth. See Using cursors to navigate collections for more information.

Example Values: 12893764510938

### Allows one to enable or<br/>
> disable retweets and device notifications from the specified user.

#### Input Parameters
* `include_entities` - _optional_ - The entities node will not be included when set to false. Example Values: false
* `skip_status` - _optional_ - When set to either true, t or 1 statuses will not be included in the returned user objects.
* `cursor` - _optional_ - Causes the list of blocked users to be broken into pages of no more than 5000 IDs at a time. The
number of IDs returned is not guaranteed to be 5000 as suspended users are filtered out after
connections are queried. If no cursor is provided, a value of -1 will be assumed, which is the first
"page."

The response from the API will include a previous_cursor and next_cursor to allow paging back and
forth. See Using cursors to navigate collections for more information.

Example Values: 12893764510938

### Returns the 20 most recent<br/>
> direct messages sent to the authenticating user. Includes detailed information about the sender and<br/>
> recipient user. You can request up to 200 direct messages per call, up to a maximum of 800 incoming<br/>
> DMs.<br/>
> <br/>
> Important: This method requires an access token with RWD (read, write and direct message)<br/>
> permissions.<br/>
> Consult The Application Permission Model for more information.

#### Input Parameters
* `count` - _optional_ - Specifies the number of direct messages to try and retrieve, up to a maximum of 200. The value of
count is best thought of as a limit to the number of Tweets to return because suspended or deleted
content is removed after the count has been applied.

Example Values: 5
* `since_id` - _optional_ - Returns results with an ID greater than (that is, more recent than) the specified ID. There are
limits to the number of Tweets which can be accessed through the API. If the limit of Tweets has
occured since the since_id, the since_id will be forced to the oldest ID available.
Example Values: 12345
* `max_id` - _optional_ - Returns results with an ID less than (that is, older than) or equal to the specified ID.

Example Values: 54321
* `include_entities` - _optional_ - The entities node will not be included when set to false.

Example Values: false
* `page` - _optional_ - Specifies the page of results to retrieve.

Example Values: 3
* `skip_status` - _optional_ - When set to either true, t or 1 statuses will not be included in the returned user objects.

### Destroys the direct<br/>
> message specified in the required ID parameter. The authenticating user must be the recipient of the<br/>
> specified direct message.<br/>
> <br/>
> Important: This method requires an access token with RWD (read, write and direct message)<br/>
> permissions.<br/>
> Consult The Application Permission Model for more information.

#### Input Parameters
* `id` - _required_ - The ID of the direct message to delete.

Example Values: 1270516771
* `include_entities` - _optional_ - The entities node will not be included when set to false.

Example Values: false

### Sends a new direct<br/>
> message to the specified user from the authenticating user. Requires both the user and text<br/>
> parameters and must be a POST. Returns the sent message in the requested format if successful.

#### Input Parameters
* `text` - _required_ - The text of your direct message. Be sure to URL encode as necessary, and keep the message under 140
characters.

Example Values: Meet me behind the cafeteria after school

### Returns the 20 most<br/>
> recent direct messages sent by the authenticating user. Includes detailed information about the<br/>
> sender and recipient user. You can request up to 200 direct messages per call, up to a maximum of<br/>
> 800 outgoing DMs.<br/>
> <br/>
> Important: This method requires an access token with RWD (read, write and direct message)<br/>
> permissions. Consult The Application Permission Model for more information.

#### Input Parameters
* `count` - _optional_ - Specifies the number of direct messages to try and retrieve, up to a maximum of 200. The value of
count is best thought of as a limit to the number of Tweets to return because suspended or deleted
content is removed after the count has been applied.

Example Values: 5
* `since_id` - _optional_ - Returns results with an ID greater than (that is, more recent than) the specified ID. There are
limits to the number of Tweets which can be accessed through the API. If the limit of Tweets has
occured since the since_id, the since_id will be forced to the oldest ID available.

Example Values: 12345
* `max_id` - _optional_ - Returns results with an ID less than (that is, older than) or equal to the specified ID.

Example Values: 54321
* `include_entities` - _optional_ - The entities node will not be included when set to false.

Example Values: false
* `page` - _optional_ - Specifies the page of results to retrieve.

Example Values: 3

### Returns a single direct<br/>
> message, specified by an id parameter. Like the /1.1/direct_messages.format request, this method<br/>
> will include the user objects of the sender and recipient.<br/>
> <br/>
> Important: This method requires an access token with RWD (read, write and direct message)<br/>
> permissions.<br/>
> Consult The Application Permission Model for more information.

#### Input Parameters
* `id` - _required_ - The ID of the direct message.

Example Values: 587424932

### Favorites the status<br/>
> specified in the ID parameter as the authenticating user. Returns the favorite status when<br/>
> successful.<br/>
> <br/>
> This process invoked by this method is asynchronous. The immediately returned status may not<br/>
> indicate the resultant favorited status of the tweet. A 200 OK response from this method will<br/>
> indicate whether the intended action was successful or not.

#### Input Parameters
* `id` - _required_ - The numerical ID of the desired status.

Example Values: 123
* `include_entities` - _optional_ - The entities node will be omitted when set to false.

Example Values: false

### Un-favorites the status<br/>
> specified in the ID parameter as the authenticating user. Returns the un-favorited status in the<br/>
> requested format when successful.<br/>
> <br/>
> This process invoked by this method is asynchronous. The immediately returned status may not<br/>
> indicate the resultant favorited status of the tweet. A 200 OK response from this method will<br/>
> indicate whether the intended action was successful or not.

#### Input Parameters
* `id` - _required_ - The numerical ID of the desired status.

Example Values: 123
* `include_entities` - _optional_ - The entities node will be omitted when set to false.

Example Values: false

### Returns the 20 most recent<br/>
> Tweets favorited by the authenticating or specified user.

#### Input Parameters
* `count` - _optional_ - Specifies the number of records to retrieve. Must be less than or equal to 200. Defaults to 20.

Example Values: 5
* `since_id` - _optional_ - Returns results with an ID greater than (that is, more recent than) the specified ID. There are
limits to the number of Tweets which can be accessed through the API. If the limit of Tweets has
occured since the since_id, the since_id will be forced to the oldest ID available.

Example Values: 12345
* `max_id` - _optional_ - Returns results with an ID less than (that is, older than) or equal to the specified ID.

Example Values: 54321
* `include_entities` - _optional_ - The entities node will be omitted when set to false.

Example Values: false

### Returns a cursored collection<br/>
> of user IDs for every user following the specified user.<br/>
> <br/>
> At this time, results are ordered with the most recent following first -- however, this ordering is<br/>
> subject to unannounced change and eventual consistency issues. Results are given in groups of 5,000<br/>
> user IDs and multiple "pages" of results can be navigated through using the next_cursor value in<br/>
> subsequent requests. See Using cursors to navigate collections for more information.<br/>
> <br/>
> This method is especially powerful when used in conjunction with GET users/lookup, a method that<br/>
> allows you to convert user IDs into full user objects in bulk.

#### Input Parameters
* `stringify_ids` - _optional_ - Many programming environments will not consume our Tweet ids due to their size. Provide this option
to have ids returned as strings instead. Example Values: true
* `cursor` - _optional_ - Causes the list of connections to be broken into pages of no more than 5000 IDs at a time. The
number of IDs returned is not guaranteed to be 5000 as suspended users are filtered out after
connections are queried. If no cursor is provided, a value of -1 will be assumed, which is the first
"page."

The response from the API will include a previous_cursor and next_cursor to allow paging back and
forth.Example Values: 12893764510938

### Returns a cursored collection of<br/>
> user IDs for every user the specified user is following (otherwise known as their "friends").<br/>
> <br/>
> At this time, results are ordered with the most recent following first -- however, this ordering is<br/>
> subject to unannounced change and eventual consistency issues. Results are given in groups of 5,000<br/>
> user IDs and multiple "pages" of results can be navigated through using the next_cursor value in<br/>
> subsequent requests. See Using cursors to navigate collections for more information.<br/>
> <br/>
> This method is especially powerful when used in conjunction with GET users/lookup, a method that<br/>
> allows you to convert user IDs into full user objects in bulk.

#### Input Parameters
* `stringify_ids` - _optional_ - Many programming environments will not consume our Tweet ids due to their size. Provide this option
to have ids returned as strings instead. Example Values: true
* `cursor` - _optional_ - Causes the list of connections to be broken into pages of no more than 5000 IDs at a time. The
number of IDs returned is not guaranteed to be 5000 as suspended users are filtered out after
connections are queried. If no cursor is provided, a value of -1 will be assumed, which is the first
"page."

The response from the API will include a previous_cursor and next_cursor to allow paging back and
forth.Example Values: 12893764510938

### Allows the authenticating<br/>
> users to follow the user specified in the ID parameter.<br/>
> <br/>
> Returns the befriended user in the requested format when successful. Returns a string describing the<br/>
> failure condition when unsuccessful. If you are already friends with the user a HTTP 403 may be<br/>
> returned, though for performance reasons you may get a 200 OK message even if the friendship already<br/>
> exists.<br/>
> <br/>
> Actions taken in this method are asynchronous and changes will be eventually consistent.

#### Input Parameters
* `follow` - _optional_ - Enable notifications for the target user. Example Values: true

### Allows the<br/>
> authenticating<br/>
> user to unfollow the user specified in the ID parameter.<br/>
> <br/>
> Returns the unfollowed user in the requested format when successful. Returns a string describing the<br/>
> failure condition when unsuccessful.<br/>
> <br/>
> Actions taken in this method are asynchronous and changes will be eventually consistent.

### Returns the<br/>
> relationships<br/>
> of the authenticating user to the comma-separated list of up to 100 screen_names or user_ids<br/>
> provided. Values for connections can be: following, following_requested, followed_by, none.

#### Input Parameters
* `stringify_ids` - _optional_ - Many programming environments will not consume our Tweet ids due to their size. Provide this option
to have ids returned as strings instead. Example Values: true
* `cursor` - _optional_ - Causes the list of connections to be broken into pages of no more than 5000 IDs at a time. The
number of IDs returned is not guaranteed to be 5000 as suspended users are filtered out after
connections are queried. If no cursor is provided, a value of -1 will be assumed, which is the first
"page."

The response from the API will include a previous_cursor and next_cursor to allow paging back and
forth.Example Values: 12893764510938

### Returns the relationships<br/>
> of the authenticating user to the comma-separated list of up to 100 screen_names or user_ids<br/>
> provided. Values for connections can be: following, following_requested, followed_by, none.

### Returns a collection of<br/>
> numeric IDs for every protected user for whom the authenticating user has a pending follow request.

#### Input Parameters
* `stringify_ids` - _optional_ - Many programming environments will not consume our Tweet ids due to their size. Provide this option
to have ids returned as strings instead. Example Values: true
* `cursor` - _optional_ - Causes the list of connections to be broken into pages of no more than 5000 IDs at a time. The
number of IDs returned is not guaranteed to be 5000 as suspended users are filtered out after
connections are queried. If no cursor is provided, a value of -1 will be assumed, which is the first
"page."

The response from the API will include a previous_cursor and next_cursor to allow paging back and
forth.Example Values: 12893764510938

### Returns detailed information<br/>
> about the relationship between two arbitrary users.

#### Input Parameters
* `source_id` - _optional_ - The user_id of the subject user.

Example Values: 3191321
* `source_screen_name` - _optional_ - The screen_name of the subject user.

Example Values: raffi
* `target_id` - _required_ - The user_id of the target user.

Example Values: 20
* `target_screen_name` - _required_ - The screen_name of the target user.

Example Values: noradio

### Allows one to enable or<br/>
> disable retweets and device notifications from the specified user.

#### Input Parameters
* `device` - _required_ - Enable/disable device notifications from the target user. Example Values: true, false
* `retweets` - _required_ - Enable/disable retweets from the target user. Example Values: true, false

### Returns all the<br/>
> information about a known place.Example Values: df51dec6f4ee2b2c

#### Input Parameters
* `place_id` - _required_ - A place in the world. These IDs can be retrieved from geo/reverse_geocode.

Example Values: df51dec6f4ee2b2c

### Creates a new place object at the<br/>
> given latitude and longitude.<br/>
> <br/>
> Before creating a place you need to query GET geo/similar_places with the latitude, longitude and<br/>
> name of the place you wish to create. The query will return an array of places which are similar to<br/>
> the one you wish to create, and a token. If the place you wish to create isn't in the returned array<br/>
> you can use the token with this method to create a new one.

#### Input Parameters
* `attribute:street_address` - _optional_ - This parameter searches for places which have this given street address. There are other
well-known, and application specific attributes available. Custom attributes are also permitted.
Learn more about Place Attributes.

Example Values: 795%20Folsom%20St
* `callback` - _optional_ - If supplied, the response will use the JSONP format with a callback of the given name.

### Given a latitude and a<br/>
> longitude, searches for up to 20 places that can be used as a place_id when updating a status.<br/>
> <br/>
> This request is an informative call and will deliver generalized results about geography

#### Input Parameters
* `lat` - _required_ - The latitude to search around. This parameter will be ignored unless it is inside the range -90.0
to +90.0 (North is positive) inclusive. It will also be ignored if there isn't a corresponding long
parameter.

Example Values: 37.7821120598956
* `long` - _required_ - The longitude to search around. The valid ranges for longitude is -180.0 to +180.0 (East is
positive) inclusive. This parameter will be ignored if outside that range, if it is not a number, if
geo_enabled is disabled, or if there not a corresponding lat parameter.

Example Values: -122.400612831116
* `accuracy` - _optional_ - A hint on the "region" in which to search. If a number, then this is a radius in meters, but it can
also take a string that is suffixed with ft to specify feet. If this is not passed in, then it is
assumed to be 0m. If coming from a device, in practice, this value is whatever accuracy the device
has measuring its location (whether it be coming from a GPS, WiFi triangulation, etc.).

Example Values: 5ft
* `granularity` - _optional_ - This is the minimal granularity of place types to return and must be one of: poi, neighborhood,
city, admin or country. If no granularity is provided for the request neighborhood is assumed.
Setting this to city, for example, will find places which have a type of city, admin or country.

Example Values: city
* `max_results` - _optional_ - A hint as to the number of results to return. This does not guarantee that the number of results
returned will equal max_results, but instead informs how many "nearby" results to return. Ideally,
only pass in the number of places you intend to display to the user here.

Example Values: 3
* `callback` - _optional_ - If supplied, the response will use the JSONP format with a callback of the given name.

### Search for places that can be<br/>
> attached to a statuses/update. Given a latitude and a longitude pair, an IP address, or a name, this<br/>
> request will return a list of all the valid places that can be used as the place_id when updating a<br/>
> status.<br/>
> <br/>
> Conceptually, a query can be made from the user's location, retrieve a list of places, have the user<br/>
> validate the location he or she is at, and then send the ID of this location with a call to POST<br/>
> statuses/update.<br/>
> <br/>
> This is the recommended method to use find places that can be attached to statuses/update. Unlike<br/>
> GET geo/reverse_geocode which provides raw data access, this endpoint can potentially re-order<br/>
> places with regards to the user who is authenticated. This approach is also preferred for<br/>
> interactive place matching with the user.

#### Input Parameters
* `accuracy` - _optional_ - A hint on the "region" in which to search. If a number, then this is a radius in meters, but it can
also take a string that is suffixed with ft to specify feet. If this is not passed in, then it is
assumed to be 0m. If coming from a device, in practice, this value is whatever accuracy the device
has measuring its location (whether it be coming from a GPS, WiFi triangulation, etc.).

Example Values: 5ft
* `granularity` - _optional_ - This is the minimal granularity of place types to return and must be one of: poi, neighborhood,
city, admin or country. If no granularity is provided for the request neighborhood is assumed.
Setting this to city, for example, will find places which have a type of city, admin or country.

Example Values: city
* `contained_within` - _optional_ - This is the place_id which you would like to restrict the search results to. Setting this value
means only places within the given place_id will be found.

Specify a place_id. For example, to scope all results to places within "San Francisco, CA USA", you
would specify a place_id of "5a110d312052166f"

Example Values: 247f43d441defc03
* `attribute:street_address` - _optional_ - This parameter searches for places which have this given street address. There are other
well-known, and application specific attributes available. Custom attributes are also permitted.
Learn more about Place Attributes.

Example Values: 795%20Folsom%20St
* `callback` - _optional_ - If supplied, the response will use the JSONP format with a callback of the given name.

### Locates places near the<br/>
> given coordinates which are similar in name.<br/>
> <br/>
> Conceptually you would use this method to get a list of known places to choose from first. Then, if<br/>
> the desired place doesn't exist, make a request to POST geo/place to create a new one.<br/>
> <br/>
> The token contained in the response is the token needed to be able to create a new place.

#### Input Parameters
* `contained_within` - _optional_ - This is the place_id which you would like to restrict the search results to. Setting this value
means only places within the given place_id will be found.

Specify a place_id. For example, to scope all results to places within "San Francisco, CA USA", you
would specify a place_id of "5a110d312052166f"

Example Values: 247f43d441defc03
* `attribute:street_address` - _optional_ - This parameter searches for places which have this given street address. There are other
well-known, and application specific attributes available. Custom attributes are also permitted.
Learn more about Place Attributes.

Example Values: 795%20Folsom%20St
* `callback` - _optional_ - If supplied, the response will use the JSONP format with a callback of the given name.

### Returns the current<br/>
> configuration used by Twitter including twitter.com slugs which are not usernames, maximum photo<br/>
> resolutions, and t.co URL lengths.<br/>
> <br/>
> It is recommended applications request this endpoint when they are loaded, but no more than once a<br/>
> day.

### Returns the list of languages<br/>
> supported by Twitter along with their ISO 639-1 code. The ISO 639-1 code is the two letter value to<br/>
> use if you include lang with any of your requests.

### Returns Twitter's Privacy Policy

### Returns the Twitter Terms of Service<br/>
> in the requested format. These are not the same as the Developer Rules of the Road.

### Creates a new list for the<br/>
> authenticated user. Note that you can't create more than 20 lists per account.

#### Input Parameters
* `name` - _required_ - The name for the list.A list's name must start with a letter and can consist only of 25 or fewer
letters, numbers, "-", or "_" characters.
* `mode` - _optional_ - Whether your list is public or private. Values can be public or private. If no mode is specified
the list will be public.
* `description` - _optional_ - The description to give the list.

### Deletes the specified list.<br/>
> The authenticated user must own the list to be able to destroy it.

#### Input Parameters
* `owner_screen_name` - _optional_ - The screen name of the user who owns the list being requested by a slug.
* `owner_id` - _optional_ - The user ID of the user who owns the list being requested by a slug.

### Returns all lists the<br/>
> authenticating or specified user subscribes to, including their own. The user is specified using the<br/>
> user_id or screen_name parameters. If no user is given, the authenticating user is used.<br/>
> <br/>
> This method used to be GET lists in version 1.0 of the API and has been renamed for consistency with<br/>
> other call.

#### Input Parameters
* `screen_name` - _required_ - The screen name of the user for whom to return results for. Helpful for disambiguating when a valid
screen name is also a user ID.

Example Values: noradio
* `user_id` - _required_ - The ID of the user for whom to return results for. Helpful for disambiguating when a valid user ID
is also a valid screen name.

Example Values: 12345

Note:: Specifies the ID of the user to get lists from. Helpful for disambiguating when a valid user
ID is also a valid screen name.

### Returns the members of the<br/>
> specified list. Private list members will only be shown if the authenticated user owns the specified<br/>
> list.

#### Input Parameters
* `owner_screen_name` - _optional_ - The screen name of the user who owns the list being requested by a slug.
* `owner_id` - _optional_ - The user ID of the user who owns the list being requested by a slug.
* `include_entities` - _optional_ - The entities node will be disincluded when set to false.

Example Values: false
* `skip_status` - _optional_ - When set to either true, t or 1 statuses will not be included in the returned user objects.
* `cursor` - _optional_ - Causes the collection of list members to be broken into "pages" of somewhat consistent size. If no
cursor is provided, a value of -1 will be assumed, which is the first "page."

The response from the API will include a previous_cursor and next_cursor to allow paging back and
forth. See Using cursors to navigate collections for more information.

Example Values: 12893764510938

### Add a member to a list.<br/>
> The authenticated user must own the list to be able to add members to it. Note that lists can't have<br/>
> more than 500 members.

#### Input Parameters
* `owner_screen_name` - _optional_ - The screen name of the user who owns the list being requested by a slug.
* `owner_id` - _optional_ - The user ID of the user who owns the list being requested by a slug.

### Adds multiple<br/>
> members to a list, by specifying a comma-separated list of member ids or screen names. The<br/>
> authenticated user must own the list to be able to add members to it. Note that lists can't have<br/>
> more than 500 members, and you are limited to adding up to 100 members to a list at a time with this<br/>
> method.<br/>
> <br/>
> Please note that there can be issues with lists that rapidly remove and add memberships. Take care<br/>
> when using these methods such that you are not too rapidly switching between removals and adds on<br/>
> the same list.

#### Input Parameters
* `owner_screen_name` - _optional_ - The screen name of the user who owns the list being requested by a slug.
* `owner_id` - _optional_ - The user ID of the user who owns the list being requested by a slug.
* `user_id` - _optional_ - A comma separated list of user IDs, up to 100 are allowed in a single request.
* `screen_name` - _optional_ - A comma separated list of screen names, up to 100 are allowed in a single request.

### Removes the specified<br/>
> member from the list. The authenticated user must be the list's owner to remove members from the<br/>
> list.

#### Input Parameters
* `list_id` - _required_ - The numerical id of the list.
* `slug` - _required_ - You can identify a list by its slug instead of its numerical id. If you decide to do so, note
that you'll also have to specify the list owner using the owner_id or owner_screen_name
parameters.
* `owner_screen_name` - _optional_ - The screen name of the user who owns the list being requested by a slug.
* `owner_id` - _optional_ - The user ID of the user who owns the list being requested by a slug.
* `user_id` - _optional_ - The ID of the user to remove from the list. Helpful for disambiguating when a valid user ID is also
a valid screen name.
* `screen_name` - _optional_ - The screen name of the user for whom to remove from the list. Helpful for disambiguating when a
valid screen name is also a user ID.

### Removes multiple<br/>
> members from a list, by specifying a comma-separated list of member ids or screen names. The<br/>
> authenticated user must own the list to be able to remove members from it. Note that lists can't<br/>
> have more than 500 members, and you are limited to removing up to 100 members to a list at a time<br/>
> with this method.<br/>
> <br/>
> Please note that there can be issues with lists that rapidly remove and add memberships. Take care<br/>
> when using these methods such that you are not too rapidly switching between removals and adds on<br/>
> the same list.

#### Input Parameters
* `owner_screen_name` - _optional_ - The screen name of the user who owns the list being requested by a slug.
* `owner_id` - _optional_ - The user ID of the user who owns the list being requested by a slug.
* `screen_name` - _optional_ - A comma separated list of screen names, up to 100 are allowed in a single request.
* `user_id` - _optional_ - A comma separated list of user IDs, up to 100 are allowed in a single request.

### Check if the specified<br/>
> user is a member of the specified list.

#### Input Parameters
* `owner_screen_name` - _optional_ - The screen name of the user who owns the list being requested by a slug.
* `owner_id` - _optional_ - The user ID of the user who owns the list being requested by a slug.
* `include_entities` - _optional_ - When set to either true, t or 1, each tweet will include a node called "entities". This node offers
a variety of metadata about the tweet in a discreet structure, including: user_mentions, urls, and
hashtags. While entities are opt-in on timelines at present, they will be made a default component
of output in the future.
* `skip_status` - _optional_ - When set to either true, t or 1 statuses will not be included in the returned user objects.

### Returns the lists the<br/>
> specified user has been added to. If user_id or screen_name are not provided the memberships for the<br/>
> authenticating user are returned.

#### Input Parameters
* `user_id` - _optional_ - The ID of the user for whom to return results for. Helpful for disambiguating when a valid user ID
is also a valid screen name.
* `screen_name` - _optional_ - The screen name of the user for whom to return results for. Helpful for disambiguating when a valid
screen name is also a user ID.
* `cursor` - _optional_ - Breaks the results into pages. A single page contains 20 lists. Provide a value of -1 to begin
paging. Provide values as returned in the response body's next_cursor and previous_cursor attributes
to page back and forth in the list.
* `filter_to_owned_lists` - _optional_ - When set to true, t or 1, will return just lists the authenticating user owns, and the user
represented by user_id or screen_name is a member of.

### Returns the specified list.<br/>
> Private lists will only be shown if the authenticated user owns the specified list.

#### Input Parameters
* `owner_screen_name` - _optional_ - The screen name of the user who owns the list being requested by a slug.
* `owner_id` - _optional_ - The user ID of the user who owns the list being requested by a slug.

### Returns tweet timeline for<br/>
> members of the specified list. Retweets are included by default. You can use the include_rts=false<br/>
> parameter to omit retweet objects.

#### Input Parameters
* `owner_screen_name` - _optional_ - The screen name of the user who owns the list being requested by a slug.
* `owner_id` - _optional_ - The user ID of the user who owns the list being requested by a slug.
* `since_id` - _optional_ - Returns results with an ID greater than (that is, more recent than) the specified ID. There are
limits to the number of Tweets which can be accessed through the API. If the limit of Tweets has
occured since the since_id, the since_id will be forced to the oldest ID available.
* `max_id` - _optional_ - Returns results with an ID less than (that is, older than) or equal to the specified ID.
* `count` - _optional_ - Specifies the number of results to retrieve per "page.
* `include_entities` - _optional_ - Entities are ON by default in API 1.1, each tweet includes a node called "entities". This node
offers a variety of metadata about the tweet in a discreet structure, including: user_mentions,
urls, and hashtags. You can omit entities from the result by using include_entities=false
* `include_rts` - _required_ - When set to either true, t or 1, the list timeline will contain native retweets (if they exist) in
addition to the standard stream of tweets. The output format of retweeted tweets is identical to the
representation you see in home_timeline.

### Returns the subscribers of<br/>
> the specified list. Private list subscribers will only be shown if the authenticated user owns the<br/>
> specified list.

#### Input Parameters
* `owner_screen_name` - _optional_ - The screen name of the user who owns the list being requested by a slug.
* `owner_id` - _optional_ - The user ID of the user who owns the list being requested by a slug.
* `cursor` - _optional_ - Breaks the results into pages. A single page contains 20 lists. Provide a value of -1 to begin
paging. Provide values as returned in the response body's next_cursor and previous_cursor attributes
to page back and forth in the list.
* `include_entities` - _optional_ - When set to either true, t or 1, each tweet will include a node called "entities". This node offers
a variety of metadata about the tweet in a discreet structure, including: user_mentions, urls, and
hashtags. While entities are opt-in on timelines at present, they will be made a default component
of output in the future. See Tweet Entities for more details.
* `skip_status` - _optional_ - When set to either true, t or 1 statuses will not be included in the returned user objects.

### Subscribes the<br/>
> authenticated user to the specified list.

#### Input Parameters
* `owner_screen_name` - _optional_ - The screen name of the user who owns the list being requested by a slug.
* `owner_id` - _optional_ - The user ID of the user who owns the list being requested by a slug.

### Unsubscribes the<br/>
> authenticated user from the specified list.

#### Input Parameters
* `owner_screen_name` - _optional_ - The screen name of the user who owns the list being requested by a slug.
* `owner_id` - _optional_ - The user ID of the user who owns the list being requested by a slug.

### Check if the specified<br/>
> user is a subscriber of the specified list. Returns the user if they are subscriber.

#### Input Parameters
* `owner_screen_name` - _optional_ - The screen name of the user who owns the list being requested by a slug.
* `owner_id` - _optional_ - The user ID of the user who owns the list being requested by a slug.
* `include_entities` - _optional_ - When set to either true, t or 1, each tweet will include a node called "entities". This node offers
a variety of metadata about the tweet in a discreet structure, including: user_mentions, urls, and
hashtags. While entities are opt-in on timelines at present, they will be made a default component
of output in the future. See Tweet Entities for more details.
* `skip_status` - _optional_ - When set to either true, t or 1 statuses will not be included in the returned user objects.

### Obtain a collection of<br/>
> the lists the specified user is subscribed to, 20 lists per page by default. Does not include the<br/>
> user's own lists.

#### Input Parameters
* `count` - _optional_ - The amount of results to return per page. Defaults to 20. Maximum of 1,000 when using cursors.
* `cursor` - _optional_ - Breaks the results into pages. A single page contains 20 lists. Provide a value of -1 to begin
paging. Provide values as returned in the response body's next_cursor and previous_cursor attributes
to page back and forth in the list. It is recommended to always use cursors when the method supports
them.

### Updates the specified list. The<br/>
> authenticated user must own the list to be able to update it.

#### Input Parameters
* `owner_screen_name` - _optional_ - The screen name of the user who owns the list being requested by a slug.
* `owner_id` - _optional_ - The user ID of the user who owns the list being requested by a slug.
* `name` - _optional_ - The name for the list.
* `mode` - _optional_ - Whether your list is public or private. Values can be public or private. If no mode is specified
the list will be public.
* `description` - _optional_ - The description to give the list.

### Create a new saved<br/>
> search for the authenticated user. A user may only have 25 saved searches.

#### Input Parameters
* `query` - _required_ - The query of the search the user would like to save.

### Destroys a<br/>
> saved<br/>
> search for the authenticating user. The authenticating user must be the owner of saved search id<br/>
> being destroyed.

#### Input Parameters
* `id` - _required_ - The ID of the saved search.

Example Values: 313006

### Returns the authenticated<br/>
> user's saved search queries.

### Returns the<br/>
> authenticated user's saved search queries.

#### Input Parameters
* `id` - _required_ - The ID of the saved search.

Example Values: 313006

### Returns a collection of<br/>
> relevant Tweets matching a specified query.<br/>
> <br/>
> Please note that Twitter's search service and, by extension, the Search API is not meant to be an<br/>
> exhaustive source of Tweets. Not all Tweets will be indexed or made available via the search<br/>
> interface.<br/>
> <br/>
> In API v1.1, the response format of the Search API has been improved to return Tweet objects more<br/>
> similar to the objects you'll find across the REST API and platform. You may need to tolerate some<br/>
> inconsistencies and variance in perspectival values (fields that pertain to the perspective of the<br/>
> authenticating user) and embedded user objects.

#### Input Parameters
* `q` - _required_ - A UTF-8, URL-encoded search query of 1,000 characters maximum, including operators. Queries may
additionally be limited by complexity.Example: @noradio.
* `geocode` - _optional_ - Returns tweets by users located within a given radius of the given latitude/longitude. The location
is preferentially taking from the Geotagging API, but will fall back to their Twitter profile. The
parameter value is specified by "latitude,longitude,radius", where radius units must be specified as
either "mi" (miles) or "km" (kilometers). Note that you cannot use the near operator via the API to
geocode arbitrary locations; however you can use this geocode parameter to search near geocodes
directly. A maximum of 1,000 distinct "sub-regions" will be considered when using the radius
modifier.
* `lang` - _optional_ - Restricts tweets to the given language, given by an ISO 639-1 code. Language detection is
best-effort.Example Values: eu
* `locale` - _optional_ - Specify the language of the query you are sending (only ja is currently effective). This is
intended for language-specific consumers and the default should work in the majority of
cases.Example Values: ja
* `result_type` - _optional_ - Optional. Specifies what type of search results you would prefer to receive. The current default is
"mixed." Valid values include:
* mixed: Include both popular and real time results in the response.
* recent: return only the most recent results in the response
* popular: return only the most popular results in the response. Example Values: mixed, recent,
popular
* `count` - _optional_ - The number of tweets to return per page, up to a maximum of 100. Defaults to 15. This was formerly
the "rpp" parameter in the old Search API. Example Values: 100
* `until` - _optional_ - Returns tweets generated before the given date. Date should be formatted as YYYY-MM-DD. Keep in
mind that the search index may not go back as far as the date you specify here. Example Values:
2012-09-01
* `since_id` - _optional_ - Returns results with an ID greater than (that is, more recent than) the specified ID. There are
limits to the number of Tweets which can be accessed through the API. If the limit of Tweets has
occured since the since_id, the since_id will be forced to the oldest ID available. Example Values:
12345
* `max_id` - _optional_ - Returns results with an ID less than (that is, older than) or equal to the specified ID. Example
Values: 12345
* `include_entities` - _optional_ - The entities node will be disincluded when set to false. Example Values: false
* `callback` - _optional_ - If supplied, the response will use the JSONP format with a callback of the given name. The
usefulness of this parameter is somewhat diminished by the requirement of authentication for
requests to this endpoint. Example Values: processTweets

### Destroys the status<br/>
> specified by the required ID parameter. The authenticating user must be the author of the specified<br/>
> status. Returns the destroyed status if successful.

#### Input Parameters
* `id` - _required_ - The numerical ID of the desired status.
* `trim_user` - _optional_ - When set to either true, t or 1, each tweet returned in a timeline will include a user object
including only the status authors numerical ID. Omit this parameter to receive the complete user
object.

### Returns a collection<br/>
> of the most recent Tweets and retweets posted by the authenticating user and the users they follow.<br/>
> The home timeline is central to how most users interact with the Twitter service.<br/>
> <br/>
> Up to 800 Tweets are obtainable on the home timeline. It is more volatile for users that follow many<br/>
> users or follow users who tweet frequently.

#### Input Parameters
* `count` - _optional_ - Specifies the number of records to retrieve. Must be less than or equal to 200.
* `max_id` - _optional_ - Returns results with an ID less than (that is, older than) or equal to the specified ID.
* `since_id` - _optional_ - Returns results with an ID greater than (that is, more recent than) the specified ID. There are
limits to the number of Tweets which can be accessed through the API. If the limit of Tweets has
occured since the since_id, the since_id will be forced to the oldest ID available.
* `trim_user` - _optional_ - When set to either true, t or 1, each tweet returned in a timeline will include a user object
including only the status authors numerical ID. Omit this parameter to receive the complete user
object.
* `exclude_replies` - _optional_ - This parameter will prevent replies from appearing in the returned timeline. Using exclude_replies
with the count parameter will mean you will receive up-to count tweets -- this is because the count
parameter retrieves that many tweets before filtering out retweets and replies.
* `contributor_details` - _optional_ - This parameter enhances the contributors element of the status response to include the screen_name
of the contributor. By default only the user_id of the contributor is included.

### Returns the 20<br/>
> most recent mentions (tweets containing a users's @screen_name) for the authenticating user.The<br/>
> timeline returned is the equivalent of the one seen when you view your mentions on twitter.com.This<br/>
> method can only return up to 800 statuses.This method will include retweets in the JSON response<br/>
> regardless of whether the include_rts parameter is set.

#### Input Parameters
* `count` - _optional_ - Specifies the number of tweets to try and retrieve, up to a maximum of 200. The value of count is
best thought of as a limit to the number of tweets to return because suspended or deleted content is
removed after the count has been applied. We include retweets in the count, even if include_rts is
not supplied. It is recommended you always send include_rts=1 when using this API method.
* `since_id` - _optional_ - Returns results with an ID greater than (that is, more recent than) the specified ID. There are
limits to the number of Tweets which can be accessed through the API. If the limit of Tweets has
occured since the since_id, the since_id will be forced to the oldest ID available.
* `max_id` - _optional_ - Returns results with an ID less than (that is, older than) or equal to the specified ID.
* `trim_user` - _optional_ - When set to either true, t or 1, each tweet returned in a timeline will include a user object
including only the status authors numerical ID. Omit this parameter to receive the complete user
object.
* `contributor_details` - _optional_ - This parameter enhances the contributors element of the status response to include the screen_name
of the contributor. By default only the user_id of the contributor is included.
* `include_entities` - _optional_ - The entities node will be disincluded when set to false.

### Returns information allowing<br/>
> the creation of an embedded representation of a Tweet on third party sites. See the oEmbed<br/>
> specification (http://oembed.com) for information about the response format. Either the id or url<br/>
> parameters must be specified in a request, it is not necessary to include both. While this endpoint<br/>
> allows a bit of customization for the final appearance of the embedded Tweet, be aware that the<br/>
> appearance of the rendered Tweet may change over time to be consistent with Twitter's Display<br/>
> Guidelines (https://dev.twitter.com/terms/display-guidelines). Do not rely on any class or id<br/>
> parameters to stay constant in the returned markup.

#### Input Parameters
* `maxwidth` - _optional_ - The maximum width in pixels that the embed should be rendered at. This value is constrained to be
between 250 and 550 pixels. Note that Twitter does not support the oEmbed maxheight parameter.
Tweets are fundamentally text, and are therefore of unpredictable height that cannot be scaled like
an image or video. Relatedly, the oEmbed response will not provide a value for height.
Implementations that need consistent heights for Tweets should refer to the hide_thread and
hide_media parameters below.
* `hide_media` - _optional_ - Specifies whether the embedded Tweet should automatically expand images which were uploaded via
POST statuses/update_with_media. When set to either true, t or
1 images will not be expanded. Defaults to false.
* `hide_thread` - _optional_ - Specifies whether the embedded Tweet should automatically show the original message in the case
that the embedded Tweet is a reply. When set to either true, t or 1 the original Tweet will not be
shown. Defaults to false.
* `omit_script` - _optional_ - Specifies whether the embedded Tweet HTML should include a
'script' element pointing to widgets.js. In cases where a page already includes widgets.js, setting
this
value to true will prevent a redundant script element from being included. When set to either true,
t or 1 the 'script'element will not be included in the embed HTML, meaning that pages must include a
reference to
widgets.js manually. Defaults to false.
* `align` - _optional_ - Specifies whether the embedded Tweet should be left aligned, right aligned, or centered in the
page. Valid values are left, right, center, and none. Defaults to none, meaning no alignment styles
are specified for the Tweet.
    Possible values: left, right, center, none.
* `related` - _optional_ - A value for the TWT related parameter, as described in Web Intents
(https://dev.twitter.com/docs/intents). This value will be forwarded to all Web Intents calls.
Example values: twitterapi, twittermedia, twitter.
* `lang` - _optional_ - Language code for the rendered embed. This will affect the text and localization of the rendered
HTML. Example value: fr

### Retweets a tweet.<br/>
> Returns<br/>
> the original tweet with retweet details embedded.

#### Input Parameters
* `id` - _required_ - The numerical ID of the desired status.
* `trim_user` - _optional_ - When set to either true, t or 1, each tweet returned in a timeline will include a user object
including only the status authors numerical ID. Omit this parameter to receive the complete user
object.

### Returns up to 100 of<br/>
> the<br/>
> first retweets of a given tweet.

#### Input Parameters
* `id` - _required_ - The numerical ID of the desired status.
* `count` - _optional_ - Specifies the number of records to retrieve. Must be less than or equal to 100.
* `trim_user` - _optional_ - When set to either true, t or 1, each tweet returned in a timeline will include a user object
including only the status authors numerical ID. Omit this parameter to receive the complete user
object.

### Returns a single status,<br/>
> specified by the id parameter below. The status's author will be returned inline.

#### Input Parameters
* `id` - _required_
* `trim_user` - _optional_ - When set to either true, t or 1, each tweet returned in a timeline will include a user object
including only the status authors numerical ID. Omit this parameter to receive the complete user
object.
* `include_my_retweet` - _optional_ - When set to either true, t or 1, any Tweets returned that have been retweeted by the authenticating
user will include an additional current_user_retweet node, containing the ID of the source status
for the retweet.
* `include_entities` - _optional_ - The entities node will be disincluded when set to false.

### Updates the authenticating<br/>
> user's status, also known as tweeting. To upload an image to accompany the tweet, use POST<br/>
> statuses/update_with_media (https://dev.twitter.com/docs/api/1/post/statuses/update_with_media). For<br/>
> each update attempt, the update text is compared with the authenticating user's recent tweets. Any<br/>
> attempt that would result in duplication will be blocked, resulting in a 403 error. Therefore, a<br/>
> user cannot submit the same status twice in a row. While not rate limited by the API a user is<br/>
> limited in the number of tweets they can create at a time. If the number of updates posted by the<br/>
> user reaches the current allowed limit this method will return an HTTP 403 error.

#### Input Parameters
* `status` - _required_ - The text of your status update, typically up to 140 characters. URL encode as necessary. t.co link
short-url wrapping (https://dev.twitter.com/docs/tco-link-wrapper/faq) may effect character counts.
* `in_reply_to_status_id` - _optional_ - The ID of an existing status that the update is in reply to. Note: This parameter will be ignored
unless the author of the tweet this parameter references is mentioned within the status text.
Therefore, you must include @username, where username is the author of the referenced tweet, within
the update.
* `lat` - _optional_ - The latitude of the location this tweet refers to. This parameter will be ignored unless it is
inside the range -90.0 to +90.0 (North is positive) inclusive. It will also be ignored if there
isn't a corresponding long parameter.
* `long` - _optional_ - The longitude of the location this tweet refers to. The valid ranges for longitude is -180.0 to
+180.0 (East is positive) inclusive. This parameter will be ignored if outside that range, if it is
not a number, if geo_enabled is disabled, or if there not a corresponding lat parameter.
* `place_id` - _optional_ - A place in the world. These IDs can be retrieved from GET geo/reverse_geocode
(https://dev.twitter.com/docs/api/1/get/geo/reverse_geocode).
* `display_coordinates` - _optional_ - Whether or not to put a pin on the exact coordinates a tweet has been sent from.
    Possible values: false, true, .
* `trim_user` - _optional_ - When set to either true, t or 1, each tweet returned in a timeline will include a user object
including only the status authors numerical ID. Omit this parameter to receive the complete user
object.

### Updates the<br/>
> authenticating user's status and attaches media for upload. Unlike POST statuses/update<br/>
> (https://dev.twitter.com/docs/api/1.1/post/statuses/update), this method expects raw multipart data.<br/>
> Your POST request's Content-Type should be set to multipart/form-data with the media[] parameter.<br/>
> The Tweet text will be rewritten to include the media URL(s), which will reduce the number of<br/>
> characters allowed in the Tweet text. If the URL(s) cannot be appended without text truncation, the<br/>
> tweet will be rejected and this method will return an HTTP 403 error. Important: Make sure that<br/>
> you're using upload.twitter.com as your host while posting statuses with media. It is strongly<br/>
> recommended to use SSL with this method.

#### Input Parameters
* `Content-Type` - _required_ - Content type.
* `media` - _required_ - Up to max_media_per_upload files may be specified in the request, each named media[]. Supported
image formats are PNG, JPG and GIF. Animated GIFs are not supported. Note: Request the GET
help/configuration (https://dev.twitter.com/docs/api/1.1/get/help/configuration) endpoint to get the
current max_media_per_upload and photo_size_limit values.
* `possibly_sensitive` - _optional_ - Set to true for content which may not be suitable for every audience.
* `in_reply_to_status_id` - _optional_ - The ID of an existing status that the update is in reply to. Note: This parameter will be ignored
unless the author of the tweet this parameter references is mentioned within the status text.
Therefore, you must include @username, where username is the author of the referenced tweet, within
the update.
* `lat` - _optional_ - The latitude of the location this tweet refers to. This parameter will be ignored unless it is
inside the range -90.0 to +90.0 (North is positive) inclusive. It will also be ignored if there
isn't a corresponding long parameter. Example value: 37.7821120598956.
* `long` - _optional_ - The longitude of the location this tweet refers to. The valid ranges for longitude is -180.0 to
+180.0 (East is positive) inclusive. This parameter will be ignored if outside that range, not a
number, geo_enabled is disabled, or if there not a corresponding lat parameter. Example value:
-122.400612831116.
* `place_id` - _optional_ - A place in the world identified by a Twitter place ID. Place IDs can be retrieved from
geo/reverse_geocode.
* `display_coordinates` - _optional_ - Whether or not to put a pin on the exact coordinates a tweet has been sent from.

### Returns the 20 most<br/>
> recent statuses posted by the authenticating user. It is also possible to request another user's<br/>
> timeline by using the screen_name or user_id parameter. The other users timeline will only be<br/>
> visible if they are not protected, or if the authenticating user's follow request was accepted by<br/>
> the protected user. The timeline returned is the equivalent of the one seen when you view a user's<br/>
> profile on twitter.com. This method can only return up to 3,200 of a user's most recent statuses.<br/>
> Native retweets of other statuses by the user is included in this total, regardless of whether<br/>
> include_rts is specified when requesting this resource. This method will not include retweets in the<br/>
> XML and JSON responses unless the include_rts parameter is set. The RSS and Atom responses will<br/>
> always include retweets as statuses prefixed with RT, regardless of provided parameters. Always<br/>
> specify either an user_id or screen_name when requesting a user timeline.

#### Input Parameters
* `count` - _optional_ - Specifies the number of tweets to try and retrieve, up to a maximum of 200. The value of count is
best thought of as a limit to the number of tweets to return because suspended or deleted content is
removed after the count has been applied. We include retweets in the count, even if include_rts is
not supplied. It is recommended you always send include_rts=1 when using this API method.
* `since_id` - _optional_ - Returns results with an ID greater than (that is, more recent than) the specified ID. There are
limits to the number of Tweets which can be accessed through the API. If the limit of Tweets has
occured since the since_id, the since_id will be forced to the oldest ID available.
* `max_id` - _optional_ - Returns results with an ID less than (that is, older than) or equal to the specified ID.
* `trim_user` - _optional_ - When set to either true, t or 1, each tweet returned in a timeline will include a user object
including only the status authors numerical ID. Omit this parameter to receive the complete user
object.
* `exclude_replies` - _optional_ - This parameter will prevent replies from appearing in the returned timeline. Using exclude_replies
with the count parameter will mean you will receive up-to count tweets -- this is because the count
parameter retrieves that many tweets before filtering out retweets and replies. This parameter is
only supported for JSON and XML responses.
* `contributor_details` - _optional_ - This parameter enhances the contributors element of the status response to include the screen_name
of the contributor. By default only the user_id of the contributor is included.
* `include_rts` - _optional_ - When set to false, the timeline will strip any native retweets (though they will still count toward
both the maximal length of the timeline and the slice selected by the count parameter). Note: If
you're using the trim_user parameter in conjunction with include_rts, the retweets will still
contain a full user object.

### Returns the locations that<br/>
> Twitter has trending topic information for.<br/>
> <br/>
> The response is an array of "locations" that encode the location's WOEID and some other<br/>
> human-readable information such as a canonical name and country the location belongs in.<br/>
> <br/>
> A WOEID is a Yahoo! Where On Earth ID.

### Returns the locations that<br/>
> Twitter has trending topic information for, closest to a specified location.<br/>
> <br/>
> The response is an array of "locations" that encode the location's WOEID and some other<br/>
> human-readable information such as a canonical name and country the location belongs in.<br/>
> <br/>
> A WOEID is a Yahoo! Where On Earth ID.

#### Input Parameters
* `lat` - _optional_ - If provided with a long parameter the available trend locations will be sorted by distance, nearest
to furthest, to the co-ordinate pair. The valid ranges for longitude is -180.0 to +180.0 (West is
negative, East is positive) inclusive.

Example Values: 37.781157
* `long` - _optional_ - If provided with a lat parameter the available trend locations will be sorted by distance, nearest
to furthest, to the co-ordinate pair. The valid ranges for longitude is -180.0 to +180.0 (West is
negative, East is positive) inclusive.

Example Values: -122.400612831116

### Returns the top 10 trending<br/>
> topics for a specific WOEID, if trending information is available for it.<br/>
> <br/>
> The response is an array of "trend" objects that encode the name of the trending topic, the query<br/>
> parameter that can be used to search for the topic on Twitter Search, and the Twitter Search URL.<br/>
> <br/>
> This information is cached for 5 minutes. Requesting more frequently than that will not return any<br/>
> more data, and will count against your rate limit usage.

#### Input Parameters
* `id` - _required_ - The Yahoo! Where On Earth ID of the location to return trending information for. Global information
is available by using 1 as the WOEID.
* `exclude` - _optional_ - Setting this equal to hashtags will remove all hashtags from the trends list.

### Returns a collection of<br/>
> users that the specified user can contribute to.

#### Input Parameters
* `include_entities` - _optional_ - The entities node will be disincluded when set to false. Example Values: false
* `skip_status` - _optional_ - When set to either true, t or 1 statuses will not be included in the returned user objects.

### Returns a collection of<br/>
> users who can contribute to the specified account.

#### Input Parameters
* `include_entities` - _optional_ - The entities node will be disincluded when set to false. Example Values: false
* `skip_status` - _optional_ - When set to either true, t or 1 statuses will not be included in the returned user objects.

### Returns fully-hydrated user<br/>
> objects for up to 100 users per request, as specified by comma-separated values passed to the<br/>
> user_id and/or screen_name parameters.<br/>
> <br/>
> This method is especially useful when used in conjunction with collections of user IDs returned from<br/>
> GET friends/ids and GET followers/ids.<br/>
> <br/>
> GET users/show is used to retrieve a single user object.

#### Input Parameters
* `screen_name` - _optional_ - A comma separated list of screen names, up to 100 are allowed in a single request. You are strongly
encouraged to use a POST for larger (up to 100 screen names) requests.

Example Values: twitterapi,twitter
* `user_id` - _optional_ - A comma separated list of user IDs, up to 100 are allowed in a single request. You are strongly
encouraged to use a POST for larger requests.

Example Values: 783214,6253282
* `include_entities` - _optional_ - The entities node that may appear within embedded statuses will be disincluded when set to false.

Example Values: false

### The user<br/>
> specified in the id is blocked by the authenticated user and reported as a spammer.

### Provides a simple,<br/>
> relevance-based search interface to public user accounts on Twitter. Try querying by topical<br/>
> interest, full name, company name, location, or other criteria. Exact match searches are not<br/>
> supported.<br/>
> <br/>
> Only the first 1,000 matching results are available.

#### Input Parameters
* `q` - _required_ - The search query to run against people search.

Example Values: Twitter%20API
* `page` - _optional_ - Specifies the page of results to retrieve.

Example Values: 3
* `count` - _optional_ - The number of potential user results to retrieve per page. This value has a maximum of 20.

Example Values: 5
* `include_entities` - _optional_ - The entities node will be disincluded when set to false.

Example Values: false

### Returns a variety of information<br/>
> about the user specified by the required user_id or screen_name parameter. The author's most recent<br/>
> Tweet will be returned inline when possible.<br/>
> <br/>
> GET users/lookup is used to retrieve a bulk collection of user objects.

#### Input Parameters
* `screen_name` - _required_ - The screen name of the user for whom to return results for. Either a id or screen_name is required
for this method.

Example Values: noradio
* `user_id` - _required_ - The ID of the user for whom to return results for. Either an id or screen_name is required for this
method.

Example Values: 12345
* `include_entities` - _optional_ - The entities node will be disincluded when set to false.

Example Values: false

### Access to Twitter's<br/>
> suggested user list. This returns the list of suggested user categories. The category can be used in<br/>
> GET users/suggestions/:slug to get the users in that category.

#### Input Parameters
* `lang` - _optional_ - Restricts the suggested categories to the requested language. The language must be specified by the
appropriate two letter ISO 639-1 representation. Currently supported languages are provided by the
GET help/languages API request. Unsupported language codes will receive English (en) results. If you
use lang in this request, ensure you also include it when requesting the GET users/suggestions/:slug
list.

### Access the users in<br/>
> a given category of the Twitter suggested user list. It is recommended that applications cache this<br/>
> data for no more than one hour.

#### Input Parameters
* `slug` - _required_ - The short name of list or a category

Example Values: twitter
* `lang` - _optional_ - Restricts the suggested categories to the requested language. The language must be specified by the
appropriate two letter ISO 639-1 representation. Currently supported languages are provided by the
GET help/languages API request. Unsupported language codes will receive English (en) results. If you
use lang in this request, ensure you also include it when requesting the GET users/suggestions/:slug
list.

### Access the<br/>
> users in a given category of the Twitter suggested user list and return their most recent status if<br/>
> they are not a protected user.

#### Input Parameters
* `slug` - _required_ - The short name of list or a category

Example Values: twitter

## License

**flow**ground :- Telekom iPaaS / twitter-com-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
