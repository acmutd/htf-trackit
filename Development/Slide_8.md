# Creating our own endpoint

Now that we've been able to get back `hello world` as a response lets try to get back `hello <name>` as a response.

Create a copy of the `template.ts` file in the `/api` folder. Rename it to be `[yourname].ts` instead so that it is unique.

### Outline

In here you should see the outline of the first function as follows

```js
export const hello_first = async (request: Request, response: Response): Promise<void> => {

}
```

When we complete this endpoint we want it to respond when we call this URL

`curl localhost:8079/hello-first-last/yourname`

=>
```json
{"message": "Hello yourname"}
```

