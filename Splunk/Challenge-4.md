# Challenge 4
Now that you know the basics of searching, let's try to add some Splunk commands to our search.

# Basic Commands

## stats count
This command can be used to count the number of a certian field. For example, let's say you wanted to find out how many requests returned 200.
```
sourcetype=access_combined_wcookie status=200 | stats count by status
```

## top
This command is used to get the field values that are the most frequent. For example, this search would get the IP address that visits the website the most.
```
sourcetype=access_combined_wcookie | top limit=1 clientip
```
In the example above, `limit=` is used to limit how many results come back.