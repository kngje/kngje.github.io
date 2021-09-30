# 安装redis
```shell
wget http://download.redis.io/releases/redis-3.0.7.tar.gz
tar zxvf redis-3.0.7.tar.gz
# ln -s 创建一个redis目录的软链接，使redis不被固定在某个版本上，便于未来redis软件版本升级
ln -s redis-3.0.7 redis
cd redis
make
make install
# 安装完成redis后 /usr/local/bin 目录下将多出几个redis开头的可执行文件
```
可执行文件 | 作用
--- | ---
redis-server | 启动redis
redis-cli | redis命令行客户端
redis-benchmark | redis基准调试工具
redis-check-aof | redis AOF 持久化文件检测和修复工具
redis-check-dump | redis RDB 持久化文件检测和修复工具
redis-sentinel | 启动redis Sentinel



# 配置redis
```shell
cd redis-x.x.x
cp -r redis.conf /opt/redis/redis.conf
#redis 配置详见:.
```

# 启动redis
```shell
redis-server /opt/redis/redis.conf
                _._                                                  
           _.-``__ ''-._                                             
      _.-``    `.  `_.  ''-._           Redis 3.0.7 (00000000/0) 64 bit
  .-`` .-```.  ```\/    _.,_ ''-._                                   
 (    '      ,       .-`  | `,    )     Running in standalone mode
 |`-._`-...-` __...-.``-._|'` _.-'|     Port: 6379
 |    `-._   `._    /     _.-'    |     PID: 17842
  `-._    `-._  `-./  _.-'    _.-'                                   
 |`-._`-._    `-.__.-'    _.-'_.-'|                                  
 |    `-._`-._        _.-'_.-'    |           http://redis.io        
  `-._    `-._`-.__.-'_.-'    _.-'                                   
 |`-._`-._    `-.__.-'    _.-'_.-'|                                  
 |    `-._`-._        _.-'_.-'    |                                  
  `-._    `-._`-.__.-'_.-'    _.-'                                   
      `-._    `-.__.-'    _.-'                                       
          `-._        _.-'                                           
              `-.__.-'  
```

# 连接redis
```shell
redis-cli [-h redis-host] [-p redis-port] [-a passwd]
#redis-host 默认是127.0.0.1
#redis-port 默认是6379
#passwd 默认无
```
