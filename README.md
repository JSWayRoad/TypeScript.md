# TypeScript.md

**TypeScript - это строго типизирвоанный язык, фактически это альтернативный синтаксис js или  
обёртка над ним, для каждой переменной или константы, для каждой функции и результатов выполнения это функции, для каждого класса, свойства и метода можно задать тип, а задав типизацию для всех  
элементов ещё на стадии написания когда, легко отследить где произошла ошибка.**

### Типы в TypeScript

Boolean, Number, String, Null, Undefined, Void(нужен для опр отсутсвющих типов)


Typescritp  add types by default for coponents so  we don't need add type for component


преимущества:   Статическая типизация. Лучшая поддержка в IDE. Доступ к новым возможностям ECMAScript.
 
**Instanceof**  
Это оператор, который работает почти так же, как typeof. Отличие только в том, что это оператор может определять не только базовые типы, но и собственные.

Enum (перечисления). Они позволяют определять именованные константы.
```
import React, { useState } from "react";

enum Status {
  Pending = "Pending",
  Success = "Success",
  Error = "Error",
}
// OR
// const Status = {
//   Pending: "Pending",
//   Success: "Success",
//   Error: "Error",
// } as const;

export const App = () => {
  const [status, setStatus] = useState(Status.Pending);

  return (
    <div>
      <p>{status}</p>
      <button onClick={() => setStatus(Status.Pending)}>
        Pending
      </button>
      <button onClick={() => setStatus(Status.Success)}>
        Success
      </button>
      <button onClick={() => setStatus(Status.Error)}>
        Error
      </button>
    </div>
  );
};
```

Дженерики (англ. generics) позволяют создавать компоненты, которые совместимы с большим количеством типов,  
а не только с одним. Это делает компоненты более «открытыми».
