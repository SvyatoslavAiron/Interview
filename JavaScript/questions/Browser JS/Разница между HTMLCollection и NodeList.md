## Разница между HTMLCollection и NodeList?

**HTMLCollection и NodeList** - это массивоподобные коллекции DOM-элементов

- NodeList может хранить любые типы узлов, а HTMLCollection - только узлы HTML элементов.

- HTMLCollection позволяет обращаться к элементам не только по индексу, но и по имени с помощью метода namedItem.

- HTMLCollection обновляется автоматически при изменении DOM, тогда как NodeList обычно статичная (кроме случаев, когда возвращается методами вроде childNodes).

NodeList, например возвращают метод `querySelectorAll()` и свойство `childNodes`, а HTMLCollection возвращают такие методы как `getElementsByTagName()` и `getElementsByClassName()`. 