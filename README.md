# Async Service Specification

It's important our asynchonous services have a standard communication stratedgy.

## Event Payloads

Event payloads should follow the `HAL` principles set out in our [API Specification](https://github.com/thisissoon/API-Specification#responses), containing only the data required for the event. If a consumer requires more data about the resource it can follow the `_link` to that resource.

``` json
{
  "_event": "track.add",
  "_timestamp": "2015-08-14T20:27:37+00:00",
  "_links": {
      "self": {
          "href": "http://api.thisissoon.fm/track/1234"
      },
      "user": {
          "href": "http://api.thisissoon.fm/user/1234",
      }
  },
  "id": "1234"
}
```