# Create Application

```
curl -H 'Authorization: NTQyODIxMDE1Njg.CaxN7w.tDYbyBKDbwox_yQo' \
     -H "Content-Type: application/json" \
     -X POST -d '{"name": "OAuth2 Test", "redirect_uris": ["http://localhost:5000/callback"]}' \
     https://discordapp.com/api/oauth2/applications
```

```
{
  "id": "152638009253036032",
  "name": "OAuth2 Test",
  "description": "",
  "icon": null,
  "secret": "p6KNMamrU5OVWtZiFe2kSkhx3Amxm0xB",
  "redirect_uris": ["http://localhost:5000/callback"],
}
```

# Run

`pip install -r requirements.txt`
`OAUTH2_CLIENT_ID=152638009253036032 OAUTH2_CLIENT_SECRET=p6KNMamrU5OVWtZiFe2kSkhx3Amxm0xB python app.py`
`open http://localhost:3000`
