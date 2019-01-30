# Component Stack

<center>
  <img src="../../assets/images/internals/components/stack.png" width="700px" alt="Apache Flink: Stack" usemap="#overview-stack">
</center>

<map name="overview-stack">
<area id="lib-datastream-cep" title="CEP: Complex Event Processing" href="/note.flink/dev/libs/cep/index.html" shape="rect" coords="63,0,143,177" />
<area id="lib-datastream-table" title="Table: Relational DataStreams" href="/note.flink/dev/table-api/index.html" shape="rect" coords="143,0,223,177" />
<area id="lib-dataset-ml" title="FlinkML: Machine Learning" href="/note.flink/dev/libs/ml/index.html" shape="rect" coords="382,2,462,176" />
<area id="lib-dataset-gelly" title="Gelly: Graph Processing" href="/note.flink/dev/libs/gelly/index.html" shape="rect" coords="461,0,541,177" />
<area id="lib-dataset-table" title="Table API and SQL" href="/note.flink/dev/table-api/index.html" shape="rect" coords="544,0,624,177" />
<area id="datastream" title="DataStream API" href="/note.flink/dev/datastream-api/index.html" shape="rect" coords="64,177,379,255" />
<area id="dataset" title="DataSet API" href="/note.flink/dev/batch/index.html" shape="rect" coords="382,177,697,255" />
<area id="runtime" title="Runtime" href="/note.flink/concepts/runtime/index.html" shape="rect" coords="63,257,700,335" />
<area id="local" title="Local" href="/note.flink/tutorials/local-setup/index.html" shape="rect" coords="62,337,275,414" />
<area id="cluster" title="Cluster" href="/note.flink/ops/deployment/cluster-setup/index.html" shape="rect" coords="273,336,486,413" />
<area id="cloud" title="Cloud" href="/note.flink/ops/deployment/gce-setup/index.html" shape="rect" coords="485,336,700,414" />
</map>

- `Deployment`：提供`Standalone`、`YARN`等部署运行方式
- `Runtime`：基于`JobGraph`，生成并行处理的数据流（其中`JobGraph`基于`DAG`表达一个`Flink`的数据流程序）
- `APIs`：基于`DataStream`（有界与无界数据流）和`DataSet`（有界数据集）的编程接口
- `Table APIs & SQL`提供以数据表（关系模型）为中心的声明式DSL和SQL编程接口
- `CEP`处理复杂事件任务，`FlinkML`处理机器学习任务，`Gelly`处理图计算任务

## Reference

- [Component Stack](https://ci.apache.org/projects/flink/flink-docs-master/internals/components.html)