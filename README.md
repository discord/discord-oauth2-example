# Create Application

Head over to our [developer site](https://discordapp.com/developers/applications/me) to create an application, and then save the `client id` and `client secret` to use in OAuth2 libraries as `client_id` and `client_secret`.

```json
{
  "id": "152638009253036032",
  "name": "OAuth2 Test",
  "description": "",
  "icon": null,
  "secret": "p6KNMamrU5OVWtZiFe2kSkhx3Amxm0xB",
  "redirect_uris": ["http://localhost:5000/callback"],
}
```

If you want to update the application then you can `PUT` to `https://discordapp.com/api/oauth2/applications/<id>` endpoint. You must include the whole object except `id` and `secret`. Icon may be set using a data-uri like the user avatar and guild icon endpoints.

# Run

- `pip install -r requirements.txt`
- `OAUTH2_CLIENT_ID=152638009253036032 OAUTH2_CLIENT_SECRET=p6KNMamrU5OVWtZiFe2kSkhx3Amxm0xB python app.py`
- `open http://localhost:5000`

# Scopes

- **identify** allows `/users/@me` without `email`.
- **email** makes `/users/@me` return an `email`.
- **connections** allows `/users/@me/connections` to return linked Twitch and YouTube accounts.
- **guilds** allows `/users/@me/guilds` to return basic information about all of a user's guilds (servers).
- **guilds.join** allows `/guilds/<guild_id>/members/<user_id>` to be used to join a guild (server).
