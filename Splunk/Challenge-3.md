# Challenge 3
Next, we'll talk about using boolean search operations and searching on specific fields to make our Splunk searches more specific.

## Searching on Fields
While we can ask Splunk to search for any log that matches the words in our search (the same way CTRL + F works), we can also take advantage of the fields that Splunk has indexed from the logs. Instead of searching for an HTTP status code like this `sourcetype="access_combined_wcookie" "HTTP 1.1\" 200"`, we can search for it like this `sourcetype="access_combined_wcookie" status=200`. Try both searches. The results should be the same.

## Boolean Searches
Let's say we want to search for both 200 and 201 status codes. We can achieve this by using an OR operator in our search like this.
```
sourcetype="access_combined_wcookie" status=200 OR status=201
```

We could also use the IN operator. It's not technically a boolean operator, but it makes this search a little easier to write.
```
sourcetype="access_combined_wcookie" status IN (200,201)
```