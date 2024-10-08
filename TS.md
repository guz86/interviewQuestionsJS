### TypeScript

https://media.licdn.com/dms/image/D4E22AQH2yk48NwwgsQ/feedshare-shrink_2048_1536/0/1716284852654?e=1719446400&v=beta&t=TtKhfMKI0RD8rsHcIPPZPLddPMkPuA_fWerjI8PMtTY

TypeScript - это язык программирования, который является надмножеством JavaScript, что означает, что любой действительный JavaScript-код также является допустимым кодом TypeScript. Вот основные различия между TypeScript и JavaScript:
1. Статическая типизация
TypeScript поддерживает статическую типизацию, что означает, что переменные, параметры функций и возвращаемые значения могут быть аннотированы с типами данных. Это позволяет обнаруживать и предотвращать ошибки типов на этапе компиляции, что улучшает безопасность и удобство разработки.

```tsx
function greet(name: string): string {
  return `Hello, ${name}!`;}
```

1. Классы и наследование
TypeScript полностью поддерживает классы и наследование, что делает его более удобным для разработки объектно-ориентированных приложений. Он предоставляет более прямой и понятный синтаксис для определения классов и методов.

```tsx
class Animal {
  name: string;  constructor(name: string) {
    this.name = name;  }
  speak(): void {
    console.log(`${this.name} makes a noise.`);  }
}
```

1. Интерфейсы
TypeScript позволяет определять интерфейсы, которые могут быть использованы для описания формы объектов. Это помогает обеспечить соответствие типов в различных частях кода и улучшает понимание структуры данных.

```tsx
interface Shape {
  color: string;}
function draw(shape: Shape): void {
  console.log(`Drawing a ${shape.color} shape.`);}
```

1. Расширенная поддержка ESNext
TypeScript поддерживает многие новые возможности JavaScript, которые были представлены в последних версиях ECMAScript, такие как стрелочные функции, шаблонные строки, деструктуризация и многое другое. Однако TypeScript также добавляет свои собственные возможности, которых нет в чистом JavaScript.
2. Транспиляция
TypeScript код не может быть напрямую исполнен в браузере, поэтому он должен быть транспилирован в обычный JavaScript перед тем, как быть выполненным в среде выполнения. Для этого используется TypeScript компилятор (tsc), который преобразует TypeScript код в эквивалентный JavaScript.

### Writing efficient TypeScript using basic types, enums, interfaces, and generics:

1. Базовые типы
TypeScript предоставляет набор базовых типов данных, таких как number, string, boolean, null, undefined и object, которые представляют основные типы данных в JavaScript.

```tsx
let num: number = 10;let str: string = 'Hello';let bool: boolean = true;let nul: null = null;let undef: undefined = undefined;let obj: object = {};
```

1. Перечисления (enums)
Перечисления в TypeScript представляют собой набор именованных числовых значений. Они помогают создавать более понятный и читаемый код, предоставляя имена для числовых значений.

```tsx
enum Direction {
  Up = 1,  Down,  Left,  Right,}
let dir: Direction = Direction.Up;console.log(dir); // Вывод: 1
```

1. Интерфейсы
Интерфейсы в TypeScript используются для определения структуры объекта. Они описывают форму объекта, указывая типы свойств и методов, которые объект должен реализовать.

```tsx
interface Person {
  name: string;  age: number;}
function greet(person: Person): void {
  console.log(`Hello, ${person.name}! You are ${person.age} years old.`);}
let user = { name: 'Alice', age: 30 };greet(user);
```

1. Обобщения (generics)
Обобщения позволяют создавать компоненты, которые могут работать с разными типами данных, сохраняя при этом тип безопасности. Они полезны для написания универсального кода, который может быть использован с различными типами данных.

```tsx
function identity<T>(arg: T): T {
  return arg;}
let output = identity<string>('hello');console.log(output); // Вывод: hello
```

Преимущества использования
Безопасность типов: Использование типов данных и интерфейсов помогает предотвратить ошибки на этапе компиляции.
Читаемость кода: Перечисления и интерфейсы делают код более понятным и облегчают его поддержку.
Гибкость и переиспользование: Обобщения позволяют писать универсальный и гибкий код, который может быть использован с различными типами данных.
Рекомендации
Используйте типы данных и интерфейсы для документирования кода и предотвращения ошибок.
Пользуйтесь перечислениями для явного определения набора значений.
Используйте обобщения для создания универсальных компонентов.

### Type vs Interface (Тип против интерфейса)

type: Позволяет создавать собственные типы данных, включая простые типы, объединения, пересечения и другие конструкции.
Позволяют создавать собственные типы данных, включая простые типы, объединения, пересечения и другие конструкции.
Поддерживают более широкий спектр возможностей, такие как операторы типов, типовые алиасы, типовые параметры и более сложные типовые выражения.
Не поддерживают наследование или объединение, но могут использоваться для создания сложных типовых структур.
Могут быть использованы в различных контекстах, включая аргументы функций, возвращаемые значения, переменные и т. д.
Позволяют определять типы для функций, которые могут содержать как объявление типов параметров, так и их реализацию.

interface: Определяет структуру объекта, но также может быть использован для описания классов, функций и других типов данных. Интерфейсы могут быть расширены и реализованы.
Интерфейсы:
Используются для определения структуры объекта, но также могут быть использованы для описания классов, функций и других типов данных.
Поддерживают наследование, что позволяет создавать иерархию интерфейсов.
Могут быть расширены другими интерфейсами с помощью оператора extends.
Используются для описания публичного контракта объекта, который может быть реализован различными объектами или классами.
Могут содержать только объявления свойств и методов, но не их реализацию.

```tsx
type Point = {
  x: number;  y: number;};interface Shape {
  color: string;  area(): number;}
```

### using interfaces with optional properties, read-only properties, etc…

- Опциональные свойства (Optional Properties)
Опциональные свойства обозначаются знаком вопроса (?) после имени свойства. Эти свойства могут быть либо указаны, либо отсутствовать в объекте, который реализует интерфейс.
Пример:

```tsx
interface User {
  name: string;  age?: number; // Опциональное свойство}
const user1: User = { name: "Alice" }; // Допустимоconst user2: User = { name: "Bob", age: 30 }; // Допустимо
```

- Свойства только для чтения (Read-Only Properties)
Свойства только для чтения обозначаются ключевым словом readonly перед именем свойства. Эти свойства могут быть установлены только при инициализации объекта и не могут быть изменены после этого.
Пример:

```tsx
interface User {
  readonly id: number; // Свойство только для чтения  name: string;  age?: number;}
const user: User = { id: 1, name: "Alice" };user.id = 2; // Ошибка: нельзя изменить свойство, только для чтения
```

- Комбинация опциональных и только для чтения свойств
Свойства могут быть одновременно и опциональными, и только для чтения.
Пример:

```tsx
Copy code
interface User {
  readonly id: number;  name: string;  readonly age?: number; // Опциональное и только для чтения свойство}
const user: User = { id: 1, name: "Alice" };user.age = 30; // Ошибка: нельзя изменить свойство, только для чтения
```

### Function Types (Типы функций)

TypeScript позволяет определять типы для функций, включая параметры и возвращаемое значение.

```tsx
type MathFunction = (x: number, y: number) => number;const add: MathFunction = (a, b) => a + b;
```

### Utility Types (Утилитарные типы) (Необязательно)

TypeScript предоставляет набор встроенных утилитарных типов, которые помогают в обработке и манипуляции типов данных.
Partial: Делает все свойства типа T необязательными.
Required: Противоположность Partial, делает все свойства типа T обязательными.
Readonly: Делает все свойства типа T только для чтения.
Record<K, T>: Создает тип, который представляет собой объект с ключами типа K и значениями типа T.
Pick<T, K>: Выбирает только определенные свойства типа T, указанные в K.
Omit<T, K>: Исключает из типа T свойства, указанные в K.
Exclude<T, U>: Создает тип, который представляет собой все типы из T, которые не находятся в U.
Extract<T, U>: Создает тип, который представляет собой все типы из T, которые находятся в U.
NonNullable: Удаляет null и undefined из типа T.
ReturnType: Получает тип возвращаемого значения функции.
Parameters: Получает тип параметров функции.
ConstructorParameters: Получает тип параметров конструктора функции.
InstanceType: Получает тип экземпляра класса или конструктора.
RequiredBy<T, K>: Делает определенные свойства типа T обязательными.
OptionalBy<T, K>: Делает определенные свойства типа T необязательными.
Это только небольшой список некоторых из наиболее часто используемых утилитарных типов в TypeScript.

### Type Guards (Типовые стражи) (Необязательно)

Типовые стражи - это конструкции в коде, которые позволяют проверить тип данных во время выполнения и обеспечить соответствующее поведение в зависимости от типа.
Функция isNumber является типовой стражей
`typeScript function isNumber(value: any): value is number {   return typeof value === 'number'; } if (isNumber(x)) {   // x имеет тип number внутри этого блока }`

### Creating Custom Types (Создание пользовательских типов)

TypeScript позволяет создавать собственные типы данных с помощью ключевого слова type.
`typeScript type Point = {   x: number;   y: number; };`

### Generic Types (Обобщенные типы) (Концепция)

Обобщенные типы позволяют создавать компоненты, которые могут работать с различными типами данных, сохраняя при этом тип безопасности.
`typeScript function identity<T>(arg: T): T {   return arg; } let output = identity<string>('hello'); let outputnumber = identity<number>(2); console.log(output); // Вывод: hello console.log(outputnumber); // Вывод: 2`

### Understanding the module system in ES6 and TypeScript.

Модульная система в ECMAScript 6 (ES6) и TypeScript позволяет разбивать код на отдельные модули или файлы, что упрощает организацию и поддержку больших проектов.
Основные концепции и возможности модульной системы в ES6 и TypeScript:
1. Объявление модулей
В ES6 и TypeScript модули могут быть объявлены с использованием ключевого слова export. Это позволяет экспортировать переменные, функции, классы и другие объекты из модуля для использования в других модулях.
`// math.ts export const sum = (a: number, b: number): number => {   return a + b; };`
2. Импортирование модулей
Для использования экспортированных объектов из других модулей используется ключевое слово import.

```
// app.ts
import { sum } from './math';
console.log(sum(2, 3)); // Вывод: 5
```

1. Экспорт по умолчанию
Модуль может экспортировать объект по умолчанию, который может быть импортирован без использования фигурных скобок.

```
// math.ts
const multiply = (a: number, b: number): number => {
 return a * b;
};
export default multiply;
// app.ts
import multiply from './math';
console.log(multiply(2, 3)); // Вывод: 6
```

1. Переименование при импорте
При импорте объектов из модуля можно переименовывать их для лучшей читаемости кода.

```
  // app.ts
import { sum as addition } from './math';
console.log(addition(2, 3)); // Вывод: 5
```

1. Экспорт и импорт всех объектов
Модуль может экспортировать и импортировать все свои объекты при помощи символа *.

```
// math.ts
export * from './constants';
export { sum, multiply } from './operations';
```

1. Использование import/export в браузере
В браузере модули могут быть загружены при помощи тега
2. Разрешение путей
TypeScript позволяет использовать различные стратегии для разрешения путей к модулям, включая относительные и абсолютные пути, а также пути, указанные в файле tsconfig.json.

```
{
  "compilerOptions": {
    "moduleResolution": "node",
    "baseUrl": "./src",
    "paths": {
      "*": ["*", "generated/*"]
    }
  }
}
```

1. Объединение модулей
TypeScript поддерживает возможность объединения модулей в один файл с помощью инструкции ///
    
    или команды компилятора –outFile.
    /// 
    ///