## Что такое декораторы в JavaScript?

**Декораторы** - это специальный синтаксис, позволяющий оборачивать и модифицировать классы, методы или свойства с помощью функции высшего порядка.

Декоратор представляют собой функцию, которая принимает в качестве аргумента целевой класс, метод или свойство и возвращает новый объект с измененной или дополнительной логикой.

Декораторы могут использоваться для добавления функциональности, такой как логирование, проверка прав доступа, кэширование и другие аспекты, не изменяя исходный код.





























<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
```
let obj = {
  mul(...rest) {
    return rest.reduce((acc, item) => acc * item, 1);
  },
};

function cachingDecoration(func) {
  const cache = new Map();

  return function (...rest) {
    const key = rest.join("*");

    if (cache.has(key)) {
      console.log("Вернул из кеша: " + cache.get(key));
      return cache.get(key);
    }

    const result = func.call(this, ...rest);
    cache.set(key, result);
    console.log(cache);

    console.log("Вычислил: " + cache.get(key));
    return result;
  };
}

obj.mul = cachingDecoration(obj.mul);

obj.mul(6, 6, 6);
```