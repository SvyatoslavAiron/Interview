## Разница между host-объектами и нативными объектами?

**Host-объекты** - это объекты, которые предоставляются средой выполнения. Например, если пишется код для браузера, то он предоставляет window, document, location, history и тому подобное.  

**Нативные объекты** - часть спецификации языка. Они доступны вне зависимости от того, на каком клиенте исполняется код.

То есть нативные объекты - часть самого языка, а хост-объекты зависят от среды выполнения (например, веб-браузера или сервера Node.js)