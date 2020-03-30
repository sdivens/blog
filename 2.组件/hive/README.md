#  hive 的基础知识

# 问题

- > FAILED: SemanticException [Error 10265]: This command is not allowed on an ACID table test_db.test_table with a non-ACID transaction manager. Failed command: null
> 
```bash
# Hive transaction manager must be set to org.apache.hadoop.hive.ql.lockmgr.DbTxnManager in order to work with ACID tables.
SET hive.txn.manager=org.apache.hadoop.hive.ql.lockmgr.DbTxnManager;

#Additionally, Set these properties to turn on transaction support
# Client Side
SET hive.support.concurrency=true;
SET hive.enforce.bucketing=true;
SET hive.exec.dynamic.partition.mode=nonstrict;

# Server Side (Metastore)
SET hive.compactor.initiator.on=true;
SET hive.compactor.worker.threads=1;

# Note: Add these properties in hive-site.xml to set them permanently.
```

# 设置spark的内存
```bash
set spark.executor.memory=8g;
```