## Что такое замыкание (Closure)?  

**Замыкание** — это комбинация функции и лексического окружения, в котором эта функция была определена.  

Такая функция имеет доступ к переменным внешней функции.  

Замыкание создаётся, когда дочерняя функция сохраняет среду родительской области видимости даже после того, как родительская функция уже выполнена.  

В JavaScript все функции изначально являются замыканиями: они автоматически запоминают, где были созданы, с помощью скрытого свойства `[[Environment]]`, и могут получить доступ к внешним переменным.