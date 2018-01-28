# 术语

**State**

表示对外部的依赖（Dependence）和影响（Effect），这里是存储依赖和影响的数据，一般是隐式的（Implicit）、透明的（Transparent）

既然是数据或结构，就需要考虑存储和访问（StateBackend）、备份和恢复（Checkpoint）等

- 幂等性：执行一次与多次的影响是一致的
- 纯函数：相同的输入，产生相同的输出，无副作用，是幂等的

**Time**

![Time](assets/images/programming-model/event_ingestion_processing_time.svg)

- 事件时间（Event Time）
- 摄入时间（Ingestion Time）
- 处理时间（Processing Time）

**Watermark**

## Reference