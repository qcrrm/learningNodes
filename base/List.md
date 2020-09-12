## ArrayList

ArrayList底层是**数组队列**，相当于动态数组。与数组相比，它的容量能动态 增长。在添加大量元素前，应用程序可以使用ensureCapacity操作来增加ArrayList实例的容量，可以减少递增式再分配的数量。







## LinkedList

-   LinkedList是一个实现了List接口和Deque接口（具有**队列**的特性）的**双端链表**。

-   底层的链表结构使它支持**高效的插入和删除操作**

-   可以调用静态类Collections类中的synchronizedList方法使其变成线程安全

    ```
    List list = Collections.synchronizedList(new linkedList(...));
    ```

    