# Creating a second endpoint

We've also set up some drivers that let you create your endpoint on ACM servers! Since you don't have your data locally, we'll be having you fill out some basic info which we'll merge into our own code.  

We'll deploy everyone's code at the end, and you will be able to request your data from us!

## Find this section in your code:

```js
//           ↓ replace this with your first and last name
export const first_last = async (request: Request, response: Response): Promise<void> => {
    const baseurl = functions.config().baseurl.firebase; // resolves to https://cloudfunctions.net
    const data = {
        email: "harshasrikara@gmail.com" // <- update with your email
    }
    const result = await axios.default.post(baseurl, data);
    const res = result.data;
    response.json({
        result: res
    });
}
```

Update the data object to have your email instead of the included one. Make sure to put the email you used to register for Hacktoberfest.

Also update the name of the function to be your own first and last name

# Linking code to endpoint

Return to the `index.ts` file and connect your endpoint to the code you just wrote. Assuming you renamed your function to `temoc_utd` you should have this as follows in your file.

```ts
import { hello_temoc, temoc_utd } from "./api/temoc"

app.get("/hello-first-last/:name", hello_first);

//add your endpoint in addition to the default one
app.get("/hello-temoc-utd/:name", hello_temoc);
app.get("/temoc-utd", temoc_utd);
```