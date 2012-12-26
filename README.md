1. ES5 features
    * Explain array methods(map, filter, some, every, reduce, reduceRight, forEach)
        
        What this code does?
        ```javascript
        
        emailsString.split( /[,;\s]+/ ).every( function( email ){
            return $u.Validator.isEmail( email );
        });
        ```
        Rewrite it with .some() method
    * Object methods
        * Describe property attributes and Object.defineProperty, Object.getOwnPropertyDescriptor methods

            Write method join:
            ```javascript
            
            var a = { 
                q: 1, 
                w: 2,
                e: 3
            };
            a.join() // output: q,w,e
            ```
            
            ```javascript
            // possible solution:
            Object.defineProperty( Object.prototype, 'join', {
                value: function(){
                    return Object.keys( this ).join( ',' );
                },
                enumerable: false
            });
            ```
        * Explain difference between Object.keys and Object.getOwnPropertyNames:
            ```javascript
            
            var a = { q: 1 };
            Object.defineProperty( a, 'xxx', {value: 'yyy', Enumerable: false} );
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
