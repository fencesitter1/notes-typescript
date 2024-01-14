**目录**

1. [视频链接](#%E8%A7%86%E9%A2%91%E9%93%BE%E6%8E%A5)
1. [介绍与赞助 (UserIntro & Sponsor)](#%E4%BB%8B%E7%BB%8D%E4%B8%8E%E8%B5%9E%E5%8A%A9%20(UserIntro%20&%20Sponsor))
1. [幻灯片 (Slides)](#%E5%B9%BB%E7%81%AF%E7%89%87%20(Slides))
1. [TypeScript 设置 (TypeScript Setup)](#TypeScript%20%E8%AE%BE%E7%BD%AE%20(TypeScript%20Setup))
1. [TSC(TSC - TypeScript Compiler)](#TSC(TSC%20-%20TypeScript%20Compiler))
	1. [执行 ts 文件输出结果](#%E6%89%A7%E8%A1%8C%20ts%20%E6%96%87%E4%BB%B6%E8%BE%93%E5%87%BA%E7%BB%93%E6%9E%9C)
1. [配置文件 (Config File)](#%E9%85%8D%E7%BD%AE%E6%96%87%E4%BB%B6%20(Config%20File))
1. [文件夹结构 (Folder Structure)](#%E6%96%87%E4%BB%B6%E5%A4%B9%E7%BB%93%E6%9E%84%20(Folder%20Structure))
1. [基本类型 (Basic Types)](#%E5%9F%BA%E6%9C%AC%E7%B1%BB%E5%9E%8B%20(Basic%20Types))
	1. [symbol](#symbol)
	1. [BigInt](#BigInt)
1. [数组与元组 (Arrays & Tuples)](#%E6%95%B0%E7%BB%84%E4%B8%8E%E5%85%83%E7%BB%84%20(Arrays%20&%20Tuples))
1. [联合类型与枚举 (Unions & Enum)](#%E8%81%94%E5%90%88%E7%B1%BB%E5%9E%8B%E4%B8%8E%E6%9E%9A%E4%B8%BE%20(Unions%20&%20Enum))
	1. [enum](#enum)
1. [对象 (Objects)](#%E5%AF%B9%E8%B1%A1%20(Objects))
1. [类型断言 (Type Assertion)](#%E7%B1%BB%E5%9E%8B%E6%96%AD%E8%A8%80%20(Type%20Assertion))
1. [函数 (Functions)](#%E5%87%BD%E6%95%B0%20(Functions))
1. [接口 (Interfaces)](#%E6%8E%A5%E5%8F%A3%20(Interfaces))
1. [函数接口 (Function Interface)](#%E5%87%BD%E6%95%B0%E6%8E%A5%E5%8F%A3%20(Function%20Interface))
	1. [与 type 的区别](#%E4%B8%8E%20type%20%E7%9A%84%E5%8C%BA%E5%88%AB)
		1. [1. **语法和用法:**](#1.%20**%E8%AF%AD%E6%B3%95%E5%92%8C%E7%94%A8%E6%B3%95:**)
		1. [2. **合并接口或类型:**](#2.%20**%E5%90%88%E5%B9%B6%E6%8E%A5%E5%8F%A3%E6%88%96%E7%B1%BB%E5%9E%8B:**)
		1. [3. **拓展（Extend）:**](#3.%20**%E6%8B%93%E5%B1%95%EF%BC%88Extend%EF%BC%89:**)
		1. [4. **实现（Implement）:**](#4.%20**%E5%AE%9E%E7%8E%B0%EF%BC%88Implement%EF%BC%89:**)
		1. [5. **可索引类型（Indexable Types）:**](#5.%20**%E5%8F%AF%E7%B4%A2%E5%BC%95%E7%B1%BB%E5%9E%8B%EF%BC%88Indexable%20Types%EF%BC%89:**)
		1. [6. **兼容性:**](#6.%20**%E5%85%BC%E5%AE%B9%E6%80%A7:**)
1. [类 (Classes)](#%E7%B1%BB%20(Classes))
1. [类的访问修饰符 (Access Modifiers)](#%E7%B1%BB%E7%9A%84%E8%AE%BF%E9%97%AE%E4%BF%AE%E9%A5%B0%E7%AC%A6%20(Access%20Modifiers))
1. [在类中实现接口 (Implement Interface in Class)](#%E5%9C%A8%E7%B1%BB%E4%B8%AD%E5%AE%9E%E7%8E%B0%E6%8E%A5%E5%8F%A3%20(Implement%20Interface%20in%20Class))
1. [扩展类（子类） (Extending Classes - Subclasses)](#%E6%89%A9%E5%B1%95%E7%B1%BB%EF%BC%88%E5%AD%90%E7%B1%BB%EF%BC%89%20(Extending%20Classes%20-%20Subclasses))
1. [泛型 (Generics)](#%E6%B3%9B%E5%9E%8B%20(Generics))
1. [TypeScript 与 React (TypeScript With React)](#TypeScript%20%E4%B8%8E%20React%20(TypeScript%20With%20React))

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
 1. **语法和用法:**
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
 2. **合并接口或类型:**
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
 3. **拓展（Extend）:**
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
 4. **实现（Implement）:**
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
5. **可索引类型（Indexable Types）:**
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
6. **兼容性:**
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
在 TypeScript 中，泛型（Generics）是一种创建可重用组件的工具，这些组件可以在多种类型上工作，而不是单一的一种类型。泛型提供了一种方式，使得组件可以适应任何数据类型。

泛型的基本语法是在函数名、类名或接口名后面加上 `<T>`，其中 `T` 是一个类型变量，它代表任何类型。在函数体、类体或接口体中，你可以像使用其他类型一样使用 `T`。

以下是一个使用泛型的函数的例子：

```typescript
function identity<T>(arg: T): T {
  return arg;
}
```

在这个例子中，`identity` 是一个泛型函数，它接收一个类型为 `T` 的参数 `arg`，并返回一个类型为 `T` 的值。你可以用任何类型来调用 `identity` 函数，例如：

```typescript
let output = identity<string>("myString");  // type of output will be 'string'
```

在这个调用中，`T` 被指定为 `string`，所以 `arg` 的类型是 `string`，返回值的类型也是 `string`。

泛型可以用于函数、类和接口，它们提供了一种灵活和可重用的方式来处理多种类型。
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

