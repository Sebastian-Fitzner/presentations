### Traditionelles I/O

``` js
var result = db.query("select name from table_person")
doSomething(result); // wait for result
doSomethingWithoutResult(); // blocked until doSomething() is done
```

### Non-Blocking I/O

``` js
db.query("select name from table_person", function(result){
doSomething(result); // wait for result
});
doSomethingWithoutResult(); // excecutes immediately
```