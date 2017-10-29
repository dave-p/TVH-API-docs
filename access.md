# access
Functions to list and manipulate access controls. With the exception of access/entry/userlist, ADMIN privilege is required to use these functions.
## passwd/entry/class
Lists the text strings, options and defaults used when configuring access controls within TVH (ie Configuration -> Users
-> Passwords). It is only likely to be needed for recreating the existing TVH GUI.
## passwd/entry/grid
Lists passwords for users. Note that "password" is in clear-text while "password2" is base64-encoded with a static prefix.
```
{
   "total" : 1,
   "entries" : [
      {
         "password" : "XxXxXxXx",
         "uuid" : "2fa9ebf7e421a537ac032a6905134137",
         "username" : "xxxxxx",
         "enabled" : true,
         "wizard" : true,
         "password2" : "Base64EncodedPassword"
}
```
## passwd/entry/create
Creates a new password record.
-   `conf` The JSON object describing the record.
## ipblock/entry/class
Lists the text strings, options and defaults used when configuring access controls within TVH (ie Configuration -> Users
-> IP Blocking Records). It is only likely to be needed for recreating the existing TVH GUI.
## ipblock/entry/grid

## ipblock/entry/create
Creates a new IP-based access record.
- `conf` The JSON object describing the access record.
## access/entry/class
Lists the text strings, options and defaults used when configuring access controls within TVH (ie Configuration -> Users
-> Access Entries). It is only likely to be needed for recreating the existing TVH GUI.
## access/entry/userlist

## access/entry/grid
Lists users and their privileges.
```
{
   "total" : 2,
   "entries" : [
      {
         "change" : [
            "change_rights",
            "change_chrange",
            "change_chtags",
            "change_dvr_configs",
            "change_profiles",
            "change_conn_limit",
            "change_lang",
            "change_lang_ui",
            "change_theme",
            "change_uilevel"
         ],
         "conn_limit" : 0,
         "admin" : false,
         "dvr_config" : [],
         "dvr" : [],
         "htsp_anonymize" : false,
         "wizard" : false,
         "profile" : [],
         "streaming" : [],
         "webui" : true,
         "channel_min" : 0,
         "channel_max" : 0,
         "uuid" : "59c300295cbf01e53f096242fd5b8ffc",
         "index" : 1,
         "lang" : "eng_GB",
         "comment" : "New entry",
         "channel_tag" : [],
         "username" : "*",
         "channel_tag_exclude" : false,
         "conn_limit_type" : 0,
         "uilevel_nochange" : 0,
         "prefix" : "192.168.0.0/24",
         "enabled" : true,
         "uilevel" : 0
      }, ...
```
## access/entry/create
Creates a new user from a JSON object.
- `conf` The JSON object describing the new user.
