1. ES5 features
    * Explain array methods(map, filter, some, every, reduce, reduceRight, forEach)
        
        What does this code do?
        ```javascript
        emailsString.split( /[,;\s]+/ ).every( email => isEmail(email) );
        ```
        
        Rewrite it with .some() method
    * Object methods
        * Describe property attributes and Object.defineProperty, Object.getOwnPropertyDescriptor methods

            Write method join:
            ```javascript
            var a = {a: 1, b: 2, c: 3};
            a.join() // output: a,b,c
            ```
            
            ```javascript
            // possible solution:
            Object.defineProperty( Object.prototype, 'join', {
                value(){
                    return Object.keys( this ).join( ',' );
                },
                enumerable: false
            });
            ```
            
        * Explain difference between Object.keys and Object.getOwnPropertyNames:
            ```javascript
            var a = {q: 1};
            Object.defineProperty( a, 'xxx', {value: 'yyy', enumerable: false} );
            Object.keys(a); // what it returns? 
            Object.getOwnPropertyNames(a); // what it returns? 
            ```
            
        * Setters and Getters
    * Strict mode restrictions
        * Global scope restrictions
        ```javascript
        (function(){
            "use strict";
            x = 100;
        })();
        ```
2. Closures
3. Context
4. Scope
    * What is the result of:
    ```javascript
    Object.prototype.x = 10;
    var y = 20;
    (function(){
        console.log( x, y );
    })();
    ```
    
5. Write function "reverse" for objects (have to work as for arrays)
    ``` javascript
    // possible solution
    function reverse( obj ){
        return Object.keys( obj ).reverse().reduce( (res, i) => {
            res[i] = obj[i];
            return res;
        }, {} );
    }
    ```
   
6. Write function "pop" for objects (have to work as for arrays)
    ``` javascript
    // possible solution
    function pop( obj ){
        var keys = Object.keys( obj );
        if ( !keys.length )
            return;
        
        var key = keys[keys.length - 1],
        val = obj[key];
        
        delete obj[key];
        return val;
    }
    ```
