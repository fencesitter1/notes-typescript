# 视频链接
[tramvelsy](https://www.youtube.com/watch?v=BCg4U1FzODs&t=46s)
# 介绍与赞助 (UserIntro & Sponsor)

# 幻灯片 (Slides)

# TypeScript 设置 (TypeScript Setup)
```shell
npm install -g typescript
```
# TSC(TSC - TypeScript Compiler)
```shell
tsc hello.ts
```
`TSC` 是 TypeScript Compiler 的缩写，是 TypeScript 的编译器工具。通过运行 `tsc` 命令，你可以将 TypeScript 代码编译成 JavaScript 代码。

下面是两种常见的 `tsc` 命令的用法：
1. **简单编译：**
   ```bash
   tsc
   ```
   这个命令会编译当前目录下的所有 TypeScript 文件（`.ts` 或 `.tsx` 文件）。

2. **监视模式：**
   ```bash
   tsc --watch
   ```
   使用 `--watch` 参数，TypeScript 编译器会进入监视模式，它将监听文件的变化，并在文件保存时自动重新编译。这对于在开发过程中保持实时编译非常有用。

   或者缩写形式：
   ```bash
   tsc -w
   ```
   
   在监视模式下，当你修改保存一个 TypeScript 文件时，编译器会自动重新编译相应的文件，使你无需手动执行 `tsc` 命令。

总之，`tsc` 是 TypeScript 编译器的命令，而 `tsc --watch` 是启用监视模式的命令，用于自动监视文件变化并重新编译。
## 执行 ts 文件输出结果
```shell
tsc
node index
```
# 配置文件 (Config File)
```shell
tsc --init
tsc --outDir  ./dist
tsc --rootDir ./src
```

# 文件夹结构 (Folder Structure)
在 TypeScript 项目中，通常会有以下两个主要文件夹：

1. **`./src` 文件夹：**
   - 这是源代码（Source Code）的存放位置。
   - 包含你编写的 TypeScript 文件（`.ts` 或 `.tsx` 文件）。

2. **`./dist` 文件夹：**
   - 这是编译后的输出目录，也称为分发目录（Distribution Directory）或输出目录。
   - 包含了经过 TypeScript 编译器处理后的 JavaScript 文件（`.js` 文件）以及可能的其他文件。
   - 当你运行 `tsc` 命令时，编译器将会把源代码从 `./src` 复制到 `./dist`，同时进行编译转换。

基本上，`./src` 是你的开发目录，你在这里编写和维护 TypeScript 代码。而 `./dist` 则是生成的目录，里面包含了编译后的 JavaScript 代码，这是最终用于运行的代码。
# 基本类型 (Basic Types)
JavaScript 的类型分为两种：原始数据类型（Primitive data types）和对象类型（Object types）。

原始数据类型包括：布尔值、数值、字符串、null、undefined 以及 ES6 中的新类型 Symbol 和 ES10 中的新类型 BigInt。
## symbol

symbol 是 JavaScript 中的一种基本数据类型，它在 ECMAScript 2015（ES6）中被引入。symbol 的主要作用是创建一个唯一且不可变的标识符。每个通过 Symbol 函数创建的 symbol 都是独一无二的，即使它们的描述文本相同。
## BigInt
BigInt 是一种内置对象，它提供了一种方法来表示大于 253 - 1的整数。BigInt 可以表示任意大的整数。
# 数组与元组 (Arrays & Tuples)
```typescript
let ids: number[] = [1, 2, 3, 4, 5];
let arr: any[] = [1, true, 'hello'];
// Tuple
let person: [number, string, boolean] = [1, 'bard', true];
person;
// Tuple Array
let employee: [number, string][] = [
  [1, 'bard'],
  [2, 'john'],
  [3, 'mike'],
];
```
# 联合类型与枚举 (Unions & Enum)
```typescript
// Union
let pid: string | number = 22;
pid = '22';

// Enum
enum Direction1 {
  Up = 'Up',
  Down = 'Down',
  Left = 'Left',
  Right = 'Right',
}

enum Direction2 {
  Up = 1,
  Down,
  Left,
  Right,
}
console.log(Direction2);//1,2,3,4
```
## enum
在 TypeScript 中，`enum` 是一种用于表示一组命名常数的数据结构。它为一组相关的值分配了符号名称，使得这些值更容易理解和使用。下面是一个简单的 `enum` 的例子：
```typescript
// 定义一个枚举类型
enum Color {
  Red,
  Green,
  Blue,
}

// 使用枚举成员
let myColor: Color = Color.Green;
console.log(myColor); // 输出: 1

// 使用枚举值
let colorName: string = Color[myColor];
console.log(colorName); // 输出: Green
```
在这个例子中，`Color` 是一个枚举类型，它包含了三个成员：`Red`、`Green` 和 `Blue`。每个成员都有一个关联的数字值，默认从 0 开始。你也可以显式地为枚举成员指定值：
```typescript
enum Color {
  Red = 1,
  Green = 2,
  Blue = 4,
}
```
在这里，`Red` 的值是 1，`Green` 的值是 2，`Blue` 的值是 4.你还可以混合使用显式和隐式赋值。

使用 `enum` 的一些注意事项：
1. **默认从 0 开始编号：** 如果你不为枚举成员指定值，它们的值将从 0 开始自动递增。
2. **可以反向映射：** 你可以使用枚举值得到对应的枚举成员名，也可以使用枚举成员名得到对应的枚举值。
   ```typescript
   enum Color {
     Red,
     Green,
     Blue,
   }

   let colorName: string = Color[1]; // 获取枚举值对应的名字
   console.log(colorName); // 输出: Green

   let colorValue: Color = Color['Green']; // 获取枚举成员名对应的值
   console.log(colorValue); // 输出: 1
   ```
3. **枚举成员可以是字符串或数字：** TypeScript 中的枚举成员可以是字符串或数字，甚至可以是混合使用。
   ```typescript
   enum Direction {
     Up = 'UP',
     Down = 'DOWN',
     Left = 1,
     Right = 2,
   }
   ```
4. **常量枚举：** 使用 `const enum` 语法可以创建常量枚举，这样在编译时会被删除，只保留枚举值。
   ```typescript
   const enum Direction {
     Up,
     Down,
     Left,
     Right,
   }

   let myDirection = Direction.Up; // 编译后直接变成常量
   ```

枚举提供了一种结构化的方式来组织一组相关的常数，并可以在代码中更加清晰地表达意图。
# 对象 (Objects)
两种定义方式
```typescript
// Objects
type user = {
  id: number;
  name: string;
}
interface User {
  id: number;
  name: string;
}
const user: User = {
  id: 1,
  name: 'John',
};
```
# 类型断言 (Type Assertion)
```typescript
let cid: any = 1;
let customerId = cid as number;
```
# 函数 (Functions)
```typescript
// Function
function addNum(x: number, y: number): number {
  return x + y;
}

console.log(addNum(1, 2));

// Void
function log(message: string | number): void {
  console.log(message);
}
```
# 接口 (Interfaces)
```typescript
// Inerfaces
interface UserInterface {
  id: number; // 只读属性
  name: string;
}
const user1: UserInterface = {
  id: 1,
  name: 'John',
};

type Point = number | string;
const p1: Point = 1;
```
# 函数接口 (Function Interface)
使用函数接口（Function Interface）来定义函数的形状，包括参数类型和返回类型。函数接口类似于对象接口，但是用于描述函数的结构。
```typescript
// Function Interface
type MathFunc = (x: number, y: number) => number;

const add: MathFunc = (x: number, y: number): number => x + y;

const sub: MathFunc = (x: number, y: number): number => x - y;
```
## 与 type 的区别
在 TypeScript 中，`interface` 和 `type` 都用于定义自定义类型，但它们之间有一些区别。下面是它们的主要区别：
### 1. **语法和用法:**
- **`interface`:**
  ```typescript
  interface Person {
    name: string;
    age: number;
  }
  ```
  `interface` 用于声明对象的结构，通常用于描述类、对象或函数签名。
- **`type`:**
  ```typescript
  type Person = {
    name: string;
    age: number;
  };
  ```
  `type` 用于声明联合类型、交叉类型，以及为现有类型起别名。
### 2. **合并接口或类型:**
- **`interface`:**
  如果你声明相同名称的两个接口，它们会自动合并成一个接口。
  ```typescript
  interface Car {
    brand: string;
  }

  interface Car {
    model: string;
  }

  // 合并后的 Car 接口
  // { brand: string; model: string; }
  ```
- **`type`:**
  对于 `type`，同名的类型声明会报错。你需要使用交叉类型 `&` 来合并类型。
  ```typescript
  type Car = {
    brand: string;
  };

  type Car = {
    model: string; // Error: Duplicate identifier 'Car'.
  };
  ```
### 3. **拓展（Extend）:**
- **`interface`:**
  `interface` 可以使用 `extends` 关键字拓展其他接口。
  ```typescript
  interface Animal {
    name: string;
  }

  interface Dog extends Animal {
    breed: string;
  }
  ```
- **`type`:**
  `type` 也可以使用 `extends` 来拓展其他类型。
  ```typescript
  type Animal = {
    name: string;
  };

  type Dog = Animal & { breed: string };
  ```
### 4. **实现（Implement）:**
- **`interface`:**
  `interface` 可以被类实现（implements）。
  ```typescript
  interface Shape {
    area(): number;
  }

  class Circle implements Shape {
    // ...
  }
  ```
- **`type`:**
  `type` 不能被类实现。
### 5. **可索引类型（Indexable Types）:**
- **`interface`:**
  `interface` 支持可索引类型。
  ```typescript
  interface StringArray {
    [index: number]: string;
  }
  ```
- **`type`:**
  `type` 也支持可索引类型。
  ```typescript
  type StringArray = {
    [index: number]: string;
  };
  ```
### 6. **兼容性:**
- **`interface`:**
  `interface` 在兼容性检查方面更宽松，允许逐渐添加成员。
- **`type`:**
  `type` 对成员的要求更为严格，不允许逐渐添加成员。

一般来说，如果你主要需要描述对象的形状，使用 `interface` 更为合适。如果你需要创建联合类型、交叉类型，或者起别名，那么 `type` 可能更适合你的需求。在实际使用中，你可能会发现两者在很多情况下可以互换使用。选择使用哪个取决于你的具体需求和个人或团队的偏好。
# 类 (Classes)
```typescript
interface PersonInterface {
  readonly: number; // 只读属性
  name: string;
  register(): string;
}
```
# 类的访问修饰符 (Access Modifiers)
TypeScript 可以使用三种访问修饰符（Access Modifiers），分别是 `public`、`private` 和 `protected`。
-  `public` 修饰的属性或方法是公有的，可以在任何地方被访问到，默认所有的属性和方法都是 public 的
-  `private` 修饰的属性或方法是私有的，不能在声明它的类的外部访问
-  `protected` 修饰的属性或方法是受保护的，它和 private 类似，区别是它在子类中也是允许被访问的
# 在类中实现接口 (Implement Interface in Class)
```typescript
class Person implements PersonInterface {
  id: number;
  name: string;
  constructor(id: number, name: string) {
    this.id = id;
    this.name = name;
  }
  register() {
    return `${this.name} is now registered`;
  }
}
const brad = new Person(1, 'brad');
const mike = new Person(2, 'mike');
console.log(brad.register()); //brad is now registered
```
# 扩展类（子类） (Extending Classes - Subclasses)
```typescript
//Subclasses extends
class Employee extends Person {
  position: string;
  constructor(id: number, name: string, position: string) {
    super(id, name);
    this.position = position;
  }
}

const emp = new Employee(3, 'brad', 'developer');
// console.log(emp.register());

```
# 泛型 (Generics)
```ts
// Generics
function getArray<T>(items: T[]): T[] {
  return new Array().concat(items);
}

let numArray = getArray<number>([1, 2, 3, 4]);
let strArray = getArray<string>(['brad', 'john', 'jane']);
let strNumArray = getArray<string | number>([
  'brad','john','jane',
  1,2,3,4,
]);
```
# TypeScript 与 React (TypeScript With React)

