# di
Simple dependency injection for TypeScript

> ```npm i reflect-metadata```
 
> ```npm i @trixis/di```

## Code example

```TypeScript
import "reflect-metadata";
import { Injectable, Inject } from "./decorators";

@Injectable()
class Service {
  test() {
    console.log("Hello world!");
  }
}

class SomeClass {
  @Inject()
  service!: Service;

  runTest() {
    this.service.test();
  }
}

const someInst = new SomeClass();
someInst.runTest(); 
```

Output: ```Hello world!```