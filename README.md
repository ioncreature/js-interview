1. ES5 features
    1. Explain array methods(map, filter, some, every, reduce, reduceRight, forEach)
        What this code does?
        emailsString.split( /[,;\s]+/ ).every( function( email ){
            return $u.Validator.isEmail( email );
        });
        Rewrite it with .some() method
    2. Object methods
        1. Describe property attributes and Object.defineProperty, Object.getOwnPropertyDescriptor methods
            Write method join:
            var a = { 
                q: 1, 
                w: 2,
                e: 3
            };
            a.join() // output: q,w,e
            
            // possible solution:
            Object.defineProperty( Object.prototype, 'join', {
                value: function(){
                    return Object.keys( this ).join( ',' );
                },
                enumerable: true
            });
        2. Explain difference between Object.keys and Object.getOwnPropertyNames:
            var a = { q: 1 };
            Object.defineProperty( a, 'xxx', {value: 'yyy', Enumerable: false} );
            Object.keys(a); // what it returns? 
            Object.getOwnPropertyNames(a); // what it returns? 
        3. Setters and Getters
    2. Strict mode restrictions
        1. Global scope restrictions
        (function(){
            "use strict";
            x = 100;
        })();
2. Closures
3. Context
4. Scope