
# Zuri Chat Core API (Data Endpoints) (1.0.0)

Connect With Us: `developer@zuri.chat` <br>
Zuri Chat is an open source slack clone. However, it offers a lot more functionality via a plugin system where each room can be provided by a different plugin provider.


# **READ ENDPOINT**

## **How it Works:**

The functionality of this endpoint is to retrieve data from the database. Data like your username, email or your phone number and some other writable data, they all can be retrieved with this endpoint.

## **How to make use of this endpoint:**

**GET **request to this URL `(https://api.zuri.chat/data/read/{plugin_id}/{coll_name}/{org_id)}`,

`for java`

```java
URL url = new URL("http://api.zuri.chat/data/read/{plugin_id}/{coll_name}/{org_id}"); HttpURLConnection con = (HttpURLConnection) url.openConnection(); con.setRequestMethod("GET");
```

`for flutter`

```dart
Future<http.Response> fetchData() {
  return http.get(Uri.parse('https://api.zuri.chat/data/read/{plugin_id}/{coll_name}/{org_id}'));
}
```

**Ensure the following required parameters have been filled:**

> `plugin_id` (required)	 provide the ID of the plugin retrieving data e.g. DM Plugin
>
> `coll_name`(required)	  provide the name of the collection to be read from e.g. DM Rooms
>
> `org_id`(required)		   provide the ID of the organization which the plugin belongs to e.g. HNGi8

## Responses

Below are the expected responses after you get after making the `get` request. You can either get a successful retrieval or an unexpected error. Below are the formats in which the responses will come.

- 200: Data Retrieved Successfully

> {
> "status": "string",
> "message": "string",
> "data": [
>  {}
> ]
> }

- default: Unexpected Error

  > {
  > "status": "string",
  > "message": "string"
  > }









