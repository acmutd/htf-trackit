# Challenge 5
Now that you know searching basics and commands, let's run through some scenarios.

# 500 Errors
Sometimes, the web requests fail and the server returns a status of 500. Is there a way you can figure out how many 500s are being returned?

# Popular Endpoints
The following search will return every endpoint the webserver handels and how many times it's been requested.
```
sourcetype=access_combined_wcookie | stats count by uri_path
```

Can you modify this search to list the top 5 uri_paths?

# Most Popular Game Category
The `categoryId` field lists the category of game the user is currently looking up. Can we create a Splunk search that will list the most popular category? What are the top 3 most popular categories?