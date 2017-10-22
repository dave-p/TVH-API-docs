# API Description
TVHeadend provides the API using the HTTP protocol, by default via port 9981 though this can be changed in the TVH config. The GET method is used, with parameters passed on the URL.

The URL must include a username and password with access permissions to carry out the requested task. If TVHeadend has been started with the '--http_root' qualifier, the HTTP root must be included in the URL, thus eg

`http://admin:admin@192.168.3.45:9981/myHttpRoot/api/config/capabilities`

The response from TVH follows the HTTP protocol and includes a status indicating successful completion or the nature of any error.

Data is usually returned as JSON, without any CR or LF characters - the examples given have been 'prettified' to make them easier to read.
