# worker queue practice

[http://nesv.github.io/golang/2014/02/25/worker-queues-in-go.html](http://nesv.github.io/golang/2014/02/25/worker-queues-in-go.html)

```bash
go build -o queued *.go

chmod +x queued

./queued -n 2048
```

New Terminal

```bash
for i in {1..4096}; do curl localhost:8000/work -d name=$USER -d delay=$(expr $i % 11)s; done
```

