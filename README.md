# interviewQuestionsJS



### что такое замыкание в JavaScript
Замыкание (closure) в JavaScript — это особенность языка, которая позволяет функции сохранять доступ к переменным из внешней области видимости, даже после завершения выполнения этой функции. Замыкания создаются тогда, когда функция определена внутри другой функции (родительской) и имеет доступ к переменным родительской функции.

Пример замыкания:

> function outerFunction() {
  var outerVariable = 10;
  function innerFunction() {
    console.log(outerVariable);
  }
  return innerFunction;
}
var closure = outerFunction();
closure(); // Выведет 10

В приведенном примере innerFunction является замыканием, потому что она определена внутри outerFunction и имеет доступ к переменной outerVariable из внешней области видимости. Когда outerFunction вызывается и возвращает innerFunction, создается замыкание closure. Затем вызов closure() сохраняет доступ к переменной outerVariable, и она может быть использована внутри innerFunction.

Замыкания в JavaScript часто используются для создания приватных переменных, сохранения состояния функции между вызовами, а также для создания функций обратного вызова и функций высшего порядка.


### Что такое Promise (Промис)?

### Что такое микро и макро таски?

### Get и POST в чем их различие?
