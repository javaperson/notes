# Redis Live

-------------------

##简介
>Redis监控工具
>[Github](https://github.com/nkrode/RedisLive)
## 安装

``` shell
pip install tornado
pip install redis
pip install python-dateutil
git clone https://github.com/kumarnitin/RedisLive.git
```
##配置
``` json
{
        "RedisServers":
        [
                {
                        "server": "10.130.110.69",
                        "port" : 6379
                },
                {
                        "server": "10.130.136.29",
                        "port" : 6379
                }
        ],

        "DataStoreType" : "sqlite",

        "SqliteStatsStore" :
        {
                "path":  "/Users/wangyang/RedisLive/src/db/redislive.sqlite"
        }
}
```
##启动
``` shell
./redis-monitor.py --duration=120
./redis-live.py
```
##访问
* http://localhost:8888/index.html
##警告
1. monitor命令会大幅降低系统吞吐量[MONITOR]http://redis.io/commands/monitor
2. duration指定监控脚本运行的时间,在次期间monitor命令一直会被执行,并且每隔1s执行一次info命令
