# Linking the code to the endpoint

Return to the `index.ts` file and connect your endpoint to the code you just wrote.

```ts
// import functions
import { hello_first, first_last } from "./api/template";

//add your import in addition to the ones above
import { hello_temoc } from "./api/temoc"

app.get("/hello-first-last/:name", hello_first);

//add your endpoint in addition to the default one
app.get("/hello-temoc-utd/:name", hello_temoc);
```

In the above code snippet we are defining a variable called `name` as anything that appears after `/hello-temoc-utd/`

# Run your code

Repeat the process to run your code and test it by calling your endpoint as such

```sh
$ curl localhost:8079/hello-temoc-utd/temoc 
{"message":"hello temoc"}
```