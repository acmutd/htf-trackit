# The code

We can retrieve the `yourname` part of the URL (also known as a query parameter) by referencing it this way `request.params.name`

Note: You'll see why the variable is called `name` in just a bit.

Fill in the function with the same code as the `/hello` endpoint but with the variable name instead. Rename the function and add your name in it. Once complete your code should appear as follows

```js
export const hello_temoc = async (request: Request, response: Response): Promise<void> => {
    const name = request.params.name; 
    response.json({
        message: `Hello ${name}`
    });
}
```
