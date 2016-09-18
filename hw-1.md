# JavaScript basic. Git. 

1. Create GitHub repo named `homeWorks` [(how?)](https://help.github.com/articles/create-a-repo/)
2. Create folder `hw-1`
3. Implement next function in separeted files
  > You could use [jsbin.com](jsbin.com) to run your code [(how?)](https://www.youtube.com/watch?v=1OsSaBuIj_g)

  ### `leftPad.js`
  
  ```javascript
  leftPad('foo', 5)
  // => "  foo" 

  leftPad('foobar', 6)
  // => "foobar" 

  leftPad(1, 2, 0)
  // => "01" 
  
  leftPad(17, 5, 0)
  // => "00017" 
  ```
  
  Create two different realizations (with strings and arrays) then compare they performance. [(how?)](http://prntscr.com/cj7lr9)
  
  ### `mapArray.js`
  
  ```javascript
  mapArray([1, 2, 3, 4], (el) => ++el)
  // => [2, 3, 4, 5]
  ```
  Function should get two params: `function mapArray(arr, fun) { ... };`
    * `arr` - Array which will be transformed
    * `fun` - Function which will transform array items one by one
  
  <b>Incoming array should be immutable! [(what?)](https://www.sitepoint.com/immutability-javascript/)</b>
  
  ### `map.js`
  This function should work like previous but first parameter also could be an object
  ```javascript 
  map([1, 2, 3, 4], (el) => ++el)
   // => [2, 3, 4, 5]
   map({a: 1, b: 2, c: 3});
   // => {a: 2, b: 3, c: 4}
   ```
   ### `flatten.js`
   Should transform array of arrays to one array where each item is a primitive 
   ```js
   flatten([1, [2, 3], [[4], [5, 6]]]);
   // => [1, 2, 3, 4, 5, 6]
   ```
   ### `fallback.js`
   Should get two params `function fallback(obj, fallback) { ... };`
      + `obj` - Object with empty field (null, '', undefined)
      + `fallback` -  First object should get his empty fields using values from this one
    ```js
    let obj = { 
     id: 0,
     info: {
      name: 'Alex',
      surname: '',
      age: null
     }, 
     description: ''
    };
      
    let fallbackObj = {
     id: 2,
     info: {
      name: 'default name',
      surname: 'default surname',
      age: 22
      },
     description: 'default description'
    }
    
    fallback(obj, fallbackObj);
      // => { id: 2, info: { name: 'Alex', surname: 'default surname', age: 22 }, description: 'default description' }
    ```
4. Add each file to separated commits at `feature/hw-1` branch
5. Push to remote and create pull request to `master` branch 
