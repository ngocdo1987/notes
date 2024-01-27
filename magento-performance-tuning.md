Ref: https://experienceleague.adobe.com/docs/commerce-operations/performance-best-practices/software.html

1/ PHP (php.ini)

memory_limit=1G

- Realpath_cache configuration
realpath_cache_size=10M
realpath_cache_ttl=7200

- ByteCode
(If high memory)
opcache.memory_consumption=512
opcache.max_accelerated_files=60000
opcache.consistency_checks=0
opcache.validate_timestamps=0
opcache.enable_cli=1

(If low memory)
opcache.memory_consumption=64
opcache.max_accelerated_files=60000

- ACPU
extension=apcu.so
[apcu]
apc.enabled = 1

2/ Nginx

https://www.nginx.com/blog/tuning-nginx/

3/ MySQL

innodb_buffer_pool_instances = 8
innodb_buffer_pool_size = 1G
max_connections = 300 -> 1000 (small -> medium)
innodb_thread_concurrency = 2 * (NumCPUs + NumDisks) => 2 * (4 + 1) = 10
