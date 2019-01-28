# Restart Strategies

- Fixed Delay Restart Strategy

作业失败后，按照指定的延迟时间和指定的重试次数，对作业进行重启尝试

```scala
val env = ExecutionEnvironment.getExecutionEnvironment()
env.setRestartStrategy(RestartStrategies.fixedDelayRestart(
  3, // The number of times that Flink retries the execution before the job is declared as failed.
  Time.of(10, TimeUnit.SECONDS) // Delaying the retry means that after a failed execution, the re-execution does not start immediately, but only after a certain delay. Delaying the retries can be helpful when the program interacts with external systems where for example connections or pending transactions should reach a timeout before re-execution is attempted.
))
```

- Failure Rate Restart Strategy

作业失败后，在指定间隔时间内，按照指定的延迟时间和指定的重试次数，对作业进行重启尝试

```scala
val env = ExecutionEnvironment.getExecutionEnvironment()
env.setRestartStrategy(RestartStrategies.failureRateRestart(
  3, // Maximum number of restarts in given time interval before failing a job
  Time.of(5, TimeUnit.MINUTES), // Time interval for measuring failure rate
  Time.of(10, TimeUnit.SECONDS) // Delay between two consecutive restart attempts
))
```

- No Restart Strategy

作业失败后，无重启尝试

```scala
val env = ExecutionEnvironment.getExecutionEnvironment()
env.setRestartStrategy(RestartStrategies.noRestart())
```

- Fallback Restart Strategy

集群默认重启策略，默认为`Fixed Delay Restart Strategy`(1 or Integer.MAX_VALUE, akka.ask.timeout or 10s)

## Reference

- [Restart Strategies](https://ci.apache.org/projects/flink/flink-docs-master/dev/restart_strategies.html)