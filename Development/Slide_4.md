# What is HTTP?

If an API is a code for computers to talk across the internet, then HTTP is the language that they speak. The hyper text transfer protocol is a common protocol that is used to structure data sent over the internet.

HTTP requests have a lot of parts. One part that most people are already familiar with is the URL. Other sections of HTTP requests are the method, request headers, and body.

### **HTTP Methods**
 - GET: To retrieve data
 - POST: To send data
 - PATCH: To update data
 - DELETE: To delete data
  
Is this an exhaustive list? No! There's many many more methods that can be used but these are the most popular options available.
### HTTP Request Breakdown
 - `GET https://wttr.in/Dallas`
 - `POST https://sendyourdata.com`
  
##### HEADER
```json
{
    "Accept-Language": "en-us",
    "Host": "github.com",
    "User-Agent": "Macintosh; Intel Mac OS X 10_15_6...",
    "Referer": "https://github.com/acmutd/htf-development",
    "Accept-Encoding": "gzip, deflate, br",
    "Connection": "keep-alive",
    "X-Requested-With": "XMLHttpRequest"
}
```
##### BODY
```json
{
    "name": "Temoc",
    "university": "UT Dallas",
    "degree": "Computer Science",
    "CC": "1234 5678 1234 5678"
}
```