## type 与 interface

https://www.edrawmax.cn/online/share.html?code=d1b8207e637811ef9fb927589a2da004

在 TypeScript 中，[`type`](command:_github.copilot.openSymbolFromReferences?%5B%22type%22%2C%5B%7B%22uri%22%3A%7B%22%24mid%22%3A1%2C%22fsPath%22%3A%22%2Fhome%2Farligle%2Fframword-study%2Fnest%2Fpackages%2Fcommon%2Finterfaces%2Fcontrollers%2Fcontroller.interface.ts%22%2C%22external%22%3A%22file%3A%2F%2F%2Fhome%2Farligle%2Fframword-study%2Fnest%2Fpackages%2Fcommon%2Finterfaces%2Fcontrollers%2Fcontroller.interface.ts%22%2C%22path%22%3A%22%2Fhome%2Farligle%2Fframword-study%2Fnest%2Fpackages%2Fcommon%2Finterfaces%2Fcontrollers%2Fcontroller.interface.ts%22%2C%22scheme%22%3A%22file%22%7D%2C%22pos%22%3A%7B%22line%22%3A0%2C%22character%22%3A7%7D%7D%5D%5D "Go to definition") 和 `interface` 都可以用来定义对象的类型，但它们有一些关键的区别和各自的使用场景。以下是它们的主要区别：

### 1. 定义方式

- **[`type`](command:_github.copilot.openSymbolFromReferences?%5B%22type%22%2C%5B%7B%22uri%22%3A%7B%22%24mid%22%3A1%2C%22fsPath%22%3A%22%2Fhome%2Farligle%2Fframword-study%2Fnest%2Fpackages%2Fcommon%2Finterfaces%2Fcontrollers%2Fcontroller.interface.ts%22%2C%22external%22%3A%22file%3A%2F%2F%2Fhome%2Farligle%2Fframword-study%2Fnest%2Fpackages%2Fcommon%2Finterfaces%2Fcontrollers%2Fcontroller.interface.ts%22%2C%22path%22%3A%22%2Fhome%2Farligle%2Fframword-study%2Fnest%2Fpackages%2Fcommon%2Finterfaces%2Fcontrollers%2Fcontroller.interface.ts%22%2C%22scheme%22%3A%22file%22%7D%2C%22pos%22%3A%7B%22line%22%3A0%2C%22character%22%3A7%7D%7D%5D%5D "Go to definition")**：使用 [`type`](command:_github.copilot.openSymbolFromReferences?%5B%22type%22%2C%5B%7B%22uri%22%3A%7B%22%24mid%22%3A1%2C%22fsPath%22%3A%22%2Fhome%2Farligle%2Fframword-study%2Fnest%2Fpackages%2Fcommon%2Finterfaces%2Fcontrollers%2Fcontroller.interface.ts%22%2C%22external%22%3A%22file%3A%2F%2F%2Fhome%2Farligle%2Fframword-study%2Fnest%2Fpackages%2Fcommon%2Finterfaces%2Fcontrollers%2Fcontroller.interface.ts%22%2C%22path%22%3A%22%2Fhome%2Farligle%2Fframword-study%2Fnest%2Fpackages%2Fcommon%2Finterfaces%2Fcontrollers%2Fcontroller.interface.ts%22%2C%22scheme%22%3A%22file%22%7D%2C%22pos%22%3A%7B%22line%22%3A0%2C%22character%22%3A7%7D%7D%5D%5D "Go to definition") 关键字定义类型别名。

  ```typescript
  type Point = {
    x: number;
    y: number;
  };
  ```

- **`interface`**：使用 `interface` 关键字定义接口。

  ```typescript
  interface Point {
    x: number;
    y: number;
  }
  ```

### 2. 扩展方式

- **[`type`](command:_github.copilot.openSymbolFromReferences?%5B%22type%22%2C%5B%7B%22uri%22%3A%7B%22%24mid%22%3A1%2C%22fsPath%22%3A%22%2Fhome%2Farligle%2Fframword-study%2Fnest%2Fpackages%2Fcommon%2Finterfaces%2Fcontrollers%2Fcontroller.interface.ts%22%2C%22external%22%3A%22file%3A%2F%2F%2Fhome%2Farligle%2Fframword-study%2Fnest%2Fpackages%2Fcommon%2Finterfaces%2Fcontrollers%2Fcontroller.interface.ts%22%2C%22path%22%3A%22%2Fhome%2Farligle%2Fframword-study%2Fnest%2Fpackages%2Fcommon%2Finterfaces%2Fcontrollers%2Fcontroller.interface.ts%22%2C%22scheme%22%3A%22file%22%7D%2C%22pos%22%3A%7B%22line%22%3A0%2C%22character%22%3A7%7D%7D%5D%5D "Go to definition")**：可以通过交叉类型（`&`）来扩展。

  ```typescript
  type Person = {
    name: string;
  };
  
  type Employee = Person & {
    employeeId: number;
  };
  ```

- **`interface`**：可以通过 `extends` 关键字来扩展。

  ```typescript
  interface Person {
    name: string;
  }
  
  interface Employee extends Person {
    employeeId: number;
  }
  ```

### 3. 合并声明

- **[`type`](command:_github.copilot.openSymbolFromReferences?%5B%22type%22%2C%5B%7B%22uri%22%3A%7B%22%24mid%22%3A1%2C%22fsPath%22%3A%22%2Fhome%2Farligle%2Fframword-study%2Fnest%2Fpackages%2Fcommon%2Finterfaces%2Fcontrollers%2Fcontroller.interface.ts%22%2C%22external%22%3A%22file%3A%2F%2F%2Fhome%2Farligle%2Fframword-study%2Fnest%2Fpackages%2Fcommon%2Finterfaces%2Fcontrollers%2Fcontroller.interface.ts%22%2C%22path%22%3A%22%2Fhome%2Farligle%2Fframword-study%2Fnest%2Fpackages%2Fcommon%2Finterfaces%2Fcontrollers%2Fcontroller.interface.ts%22%2C%22scheme%22%3A%22file%22%7D%2C%22pos%22%3A%7B%22line%22%3A0%2C%22character%22%3A7%7D%7D%5D%5D "Go to definition")**：不能合并声明。

  ```typescript
  type A = {
    x: number;
  };
  
  // 重新定义会报错
  // type A = {
  //   y: number;
  // };
  ```

- **`interface`**：可以合并声明。

  ```typescript
  interface A {
    x: number;
  }
  
  interface A {
    y: number;
  }
  
  // 合并后，A 包含 x 和 y
  const obj: A = { x: 1, y: 2 };
  ```

### 4. 使用场景

- **[`type`](command:_github.copilot.openSymbolFromReferences?%5B%22type%22%2C%5B%7B%22uri%22%3A%7B%22%24mid%22%3A1%2C%22fsPath%22%3A%22%2Fhome%2Farligle%2Fframword-study%2Fnest%2Fpackages%2Fcommon%2Finterfaces%2Fcontrollers%2Fcontroller.interface.ts%22%2C%22external%22%3A%22file%3A%2F%2F%2Fhome%2Farligle%2Fframword-study%2Fnest%2Fpackages%2Fcommon%2Finterfaces%2Fcontrollers%2Fcontroller.interface.ts%22%2C%22path%22%3A%22%2Fhome%2Farligle%2Fframword-study%2Fnest%2Fpackages%2Fcommon%2Finterfaces%2Fcontrollers%2Fcontroller.interface.ts%22%2C%22scheme%22%3A%22file%22%7D%2C%22pos%22%3A%7B%22line%22%3A0%2C%22character%22%3A7%7D%7D%5D%5D "Go to definition")**：适用于定义联合类型、交叉类型、原始类型别名、元组等。

  ```typescript
  type StringOrNumber = string | number;
  type Point = { x: number; y: number };
  type ReadOnlyPoint = Readonly<Point>;
  ```

- **`interface`**：适用于定义对象类型，尤其是需要扩展和合并声明的场景。

  ```typescript
  interface Point {
    x: number;
    y: number;
  }
  
  interface Point3D extends Point {
    z: number;
  }
  ```

### 5. 其他差异

- **[`type`](command:_github.copilot.openSymbolFromReferences?%5B%22type%22%2C%5B%7B%22uri%22%3A%7B%22%24mid%22%3A1%2C%22fsPath%22%3A%22%2Fhome%2Farligle%2Fframword-study%2Fnest%2Fpackages%2Fcommon%2Finterfaces%2Fcontrollers%2Fcontroller.interface.ts%22%2C%22external%22%3A%22file%3A%2F%2F%2Fhome%2Farligle%2Fframword-study%2Fnest%2Fpackages%2Fcommon%2Finterfaces%2Fcontrollers%2Fcontroller.interface.ts%22%2C%22path%22%3A%22%2Fhome%2Farligle%2Fframword-study%2Fnest%2Fpackages%2Fcommon%2Finterfaces%2Fcontrollers%2Fcontroller.interface.ts%22%2C%22scheme%22%3A%22file%22%7D%2C%22pos%22%3A%7B%22line%22%3A0%2C%22character%22%3A7%7D%7D%5D%5D "Go to definition")**：可以用于定义复杂类型，如联合类型、交叉类型、元组等。

  ```typescript
  type UnionType = string | number;
  type TupleType = [number, string];
  ```

- **`interface`**：主要用于定义对象的结构，不能直接用于定义联合类型或元组。

  ```typescript
  interface Point {
    x: number;
    y: number;
  }
  ```

### 总结

- 使用 [`type`](command:_github.copilot.openSymbolFromReferences?%5B%22type%22%2C%5B%7B%22uri%22%3A%7B%22%24mid%22%3A1%2C%22fsPath%22%3A%22%2Fhome%2Farligle%2Fframword-study%2Fnest%2Fpackages%2Fcommon%2Finterfaces%2Fcontrollers%2Fcontroller.interface.ts%22%2C%22external%22%3A%22file%3A%2F%2F%2Fhome%2Farligle%2Fframword-study%2Fnest%2Fpackages%2Fcommon%2Finterfaces%2Fcontrollers%2Fcontroller.interface.ts%22%2C%22path%22%3A%22%2Fhome%2Farligle%2Fframword-study%2Fnest%2Fpackages%2Fcommon%2Finterfaces%2Fcontrollers%2Fcontroller.interface.ts%22%2C%22scheme%22%3A%22file%22%7D%2C%22pos%22%3A%7B%22line%22%3A0%2C%22character%22%3A7%7D%7D%5D%5D "Go to definition") 定义复杂类型、联合类型、交叉类型、元组等。
- 使用 `interface` 定义对象类型，尤其是需要扩展和合并声明的场景。

选择 [`type`](command:_github.copilot.openSymbolFromReferences?%5B%22type%22%2C%5B%7B%22uri%22%3A%7B%22%24mid%22%3A1%2C%22fsPath%22%3A%22%2Fhome%2Farligle%2Fframword-study%2Fnest%2Fpackages%2Fcommon%2Finterfaces%2Fcontrollers%2Fcontroller.interface.ts%22%2C%22external%22%3A%22file%3A%2F%2F%2Fhome%2Farligle%2Fframword-study%2Fnest%2Fpackages%2Fcommon%2Finterfaces%2Fcontrollers%2Fcontroller.interface.ts%22%2C%22path%22%3A%22%2Fhome%2Farligle%2Fframword-study%2Fnest%2Fpackages%2Fcommon%2Finterfaces%2Fcontrollers%2Fcontroller.interface.ts%22%2C%22scheme%22%3A%22file%22%7D%2C%22pos%22%3A%7B%22line%22%3A0%2C%22character%22%3A7%7D%7D%5D%5D "Go to definition") 还是 `interface` 主要取决于具体的使用场景和需求。