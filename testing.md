## Stress Testing
* Stress testing in software is a performance testing method that evaluates how a system behaves under extreme or abnormal conditions, aiming to identify its breaking point and how it handles failures. It pushes the system beyond its expected load, like high user traffic or large-scale data processing, to determine its resilience and capacity limits. 
* Example softwares:
    * wrk: wrk is a modern HTTP benchmarking tool capable of generating significant load when run on a single multi-core CPU. It combines a multithreaded design with scalable event notification systems such as epoll and kqueue.
        * Example:
        `wrk -t12 -c400 -d30s http://127.0.0.1:8080/index.html`
        This runs a benchmark for 30 seconds, using 12 threads and keeping 400 http connections open
        * https://github.com/wg/wrk

    