# 内存设置

## JVM内存

- Heap
  - OutOfMemoryError: Java heap space
  - taskmanager.memory.task.heap.size
- Direct
  - OutOfMemoryError: Direct buffer memory
- Metaspace
  - OutOfMemoryError: Metaspace
  - taskmanager.memory.jvm-metaspace.size=256m
- Stack
- Code Cache
- Native

## 外部内存

- YARN Container
- System

## Flink

- network

  - taskmanager.memory.network.min
  - taskmanager.memory.network.max
  - taskmanager.memory.network.fraction 

- jvm overhead

  - taskmanager.memory.jvm-overhead.min
  - taskmanager.memory.jvm-overhead.max
  - taskmanager.memory.jvm-overhead.fraction 
  
# 参考

- [内存配置](https://ci.apache.org/projects/flink/flink-docs-release-1.10/zh/ops/memory/mem_setup.html)
