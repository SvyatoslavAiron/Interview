## Разница между микро и макрозадачами в event loop?

**Микрозадачи** - это отложенные задачи, которые имеют приоритет над макрозадачами, то есть после выполнения синхронного кода и перед тем как event loop перейдёт к следующей макрозадаче, он сначала выполняет все микрозадачи.

- Операции с промисами
- Метод `queueMicrotask()`

**Макрозадачи** - это крупные задачи которые добавляются в основную очередь задач. Эти задачи обрабатываются после завершения синхронного кода и всех микрозадач.

- Таймеры
- Обработчики событий
- выполнение AJAX-запросов