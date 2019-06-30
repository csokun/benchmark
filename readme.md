# NodeJS Benchmark Tools

Bundling two most popular npm packages used for performing API request benchmark `concurrently` and `autocannon`.


# Usage


```bash
docker run -it --rm csokun/benchmark:latest

concurrently "autocannon -f -c 50 localhost:3000/a" \
             "autocannon -f -c 50 localhost:3000/b" \
             "autocannon -f -c 50 localhost:3000/c"
```

or, you can launch a quick command like this:

```bash
docker run -it --rm csokun/benchmark:latest /bin/sh -c 'autocannon -f -c 1 google.com'
```

# Reference

This docker build is inspired by this blog post https://www.nearform.com/blog/how-to-build-a-real-time-node-js-performance-monitoring-system/ 
