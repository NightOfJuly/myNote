# java集合总结 #

**Map**

- HashMap继承于AbstractMap，
   实现了Map，Cloneable，java.io.Serializable接口。
- 线程不安全，底层是数组加链表实现的哈希表，映射不是有序的。
- 允许null作为键，null作为值，key不可以重复，value可以重复。
- HashMap去掉了contains方法，取而代之的是containsKey和containsValue。

