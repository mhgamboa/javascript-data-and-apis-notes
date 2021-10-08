# Javascript Data and APIs Notes

Thank you to The Coding Train for making a [Youtube playlist](https://www.youtube.com/playlist?list=PLRqwX-V7Uu6YxDKpFzf_2D84p0cyk4T7X) to teach me!!

## 1.1: fetch() - Working With Data & APIs in JavaScript

- Javascript can use `fetch()` to send requests (aka communicate) to servers
  - **Get** requests "ask" for data. **Post** requests "send" data
- `fetch()`'s first argument is the path to a resource where you are trying to acquire data
- The `response` that `fetch()` returns always needs to be parsed
  - It can be parsed into a **blob** (example is used for images), **text**, **array stream**, or **json** (Which is very important!!)

### Using `fetch()` with `.then()`

- `fetch()` can be chained with one or more `.then()` statements to resolve the `promise` that fetch returns.
- `fetch()` must also be chained with `.catch()` to handle any errors that may arrise

EX:

```
const url = ""
fetch(url).then(response => )
```

### Using `fetch()` With `async` and `await`

- You can also use async/await functions instead of `.then().catch()` chaining

  - You will still need to write a `.catch()` method.

  ```
  async myFunction = () => {
      const myFetch = await fetch(url);
      const data = await myFetch.json();
      ...
      return foo;
  }
  myFunction().catch( error => {
      console.error(error)
  })
  ```
