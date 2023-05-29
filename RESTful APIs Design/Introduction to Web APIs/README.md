## [Introduction to Web APIs](https://www.linkedin.com/learning/introduction-to-web-apis-2019) with Andrew Probert `2019 edition`

- [x]  Introduction
- [x]  1. What Is an API?
- [x]  2. Connecting to an API
- [x]  3. Working with an API
- [x]  4. Working with the Giphy API
- [x]  5. Error Handling and Security
- [x]  6. What about GraphQL?
- [x]  Conclusion

API stands for Application Programming Interface.

There are 2 main data formats to get back the API response.

- XML
- JSON

API response gets back as a String and to convert them into JavaScript Object, type `JSON.parse(response)`

```js
const request = new XMLHttpRequest();
  request.open('GET', 'https://hplussport.com/api/products?order=name');

  request.onload = function() {
      let response = request.response;
      let parsedData = JSON.parse(response);
      console.log(parsedData);

  request.send();
```

- Endpoints - Connection for an API
    - Example - myresturant.com/api/salad (salad is an endpoint)
- Parameters - Filters for the API data
    - Example - myresturant.com/api/salad?sauce=tomatos