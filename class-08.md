# Class-08 Reading Notes

### THE PAST, PRESENT & FUTURE OF LOCAL STORAGE FOR WEB APPLICATIONS

* Cookies are included with every HTTP request, thereby slowing down your web application by needlessly transmitting the same data over and over
* Cookies are included with every HTTP request, thereby sending data unencrypted over the internet
* Cookies are limited to about 4 KB of data — enough to slow down your application
* DHTML Behaviors - one of them being userData
* userData allows web pages to store up to 64 KB of data per domain
* HTML5 Storage is a specification named Web Storage
* Also sometimes refereed to as Local Storage or DOM Storage
* you can access this storage in javascript through localStorage
* HTML5 Storage is based on named key/value pairs
* Its a string that need to be parsed to be a javascript datatype
* Calling setItem() with a named key that already exists will silently overwrite the previous value
* Calling getItem() with a non-existent key will return null rather than throw an exception
* there is more to life than “5 megabytes of named key/value pairs,”