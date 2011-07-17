appengine-thumbnails
====================

Concept inspired by Simon Willison's Resize Proxy (https://github.com/simonw/resize-proxy). Allows the UI to be changed without affecting image uploads.

Set BASE_URL to your origin servers, or leave blank to allow any server. Set the dimensions allowed, or leave empty for any dimensions. Then deploy to appengine.

Images are now available on urls such as 

http://yourapp.appspot.com/w/50/h/50/q/85/upload/images/myimage.jpg if BASE_URL given.

http://yourapp.appspot.com/w/50/h/50/q/85/mysite.com/upload/images/myimage.jpg if BASE_URL not given.

Also fixed width images can be generated using

http://yourapp.appspot.com/w/50/q/85/upload/images/myimage.jpg if BASE_URL given.

It is recommended that you setup payments for appengine, as this will enable a varnish cache even if you don't go above the free quota's, speeding up the requests.

