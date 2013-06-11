# OmniAuth OAuth2 for Kaeuferportal

Create a service in KP-Backend:

`bundle exec rake service:create function=targeting2 url='http://localhost:3003'`

```
# Added "targeting2" to Services with service-url http://localhost:3003 ."
# Please add this to your service's environment configuration:
# (consider changing the :site option to suit your environment)
#

Rails.application.config.middleware.use OmniAuth::Builder do
  provider :kaeuferportal,
    "6c2a8f20b4a301300a180454530a9e51-64d3a190d945012d4b2158b035f038ab",
    "f8b24428f439b95ba6dec387198e08080e3e3bdf09129da43339d9e3bf8e680c",
    :client_options => { :site => 'http://change.this.host' }
end
```

Insert middleware into the new service app. Repeat for production.
