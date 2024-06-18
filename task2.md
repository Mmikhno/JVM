Вывод консоли:
![alt text](./image/0.png)

1. Metaspace

- 20:40:16 - 20:40:23 - загрузка классов из пакетов io.vertex, io.netty, io.springframework
  ![alt text](./image/1.png)

1. Heap

- 20:40:25 - 20:40:26 - создается 5_000_000 объектов в куче, увеличивается размер кучи:  
  List<SimpleObject> simpleObjects = createSimpleObjects(5_000_000);

![alt text](./image/2.png)

- добавляется еще 5_000_000 объектов в куче:
  simpleObjects.addAll(createSimpleObjects(5_000_000));
  ![alt text](./image/3.png)

- добавляется еще 5_000_000 объектов в куче, увеличивается размер кучи (резервируется дополнтительная память):  
  simpleObjects.addAll(createSimpleObjects(5_000_000));

![alt text](./image/4.png)
