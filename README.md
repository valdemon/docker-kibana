> **NOTE**
>
> _This is a straight fork from the excellent [khezen/docker-kibana](https://github.com/khezen/docker-kibana) work. The main difference is usage of the [Kibana OSS distribution](https://www.elastic.co/downloads/kibana-oss) instead of the [default one](https://www.elastic.co/downloads/kibana)._


# Supported tags and respective `Dockerfile` links

* [![GitHub (release)](https://img.shields.io/github/release/valdemon/docker-kibana-oss.svg)](https://github.com/valdemon/docker-kibana-oss/releases/latest) ![Tag](https://img.shields.io/badge/latest-yellowgreen.svg) [![](https://img.shields.io/badge/Dockerfile-darkred.svg)](https://github.com/valdemon/docker-kibana-oss/blob/6.5.4-17/Dockerfile) [![](https://images.microbadger.com/badges/image/valdemon/kibana-oss.svg)](https://microbadger.com/images/valdemon/kibana-oss)

# What is Kibana?
Kibana lets you visualize your Elasticsearch data and navigate the Elastic Stack, so you can do anything from learning why you're getting paged at 2:00 a.m. to understanding the impact rain might have on your quarterly numbers.

[<img src="https://static-www.elastic.co/fr/assets/blt282ae2420e32fc38/icon-kibana-bb.svg?q=802" width="144" height="144">](https://www.elastic.co/fr/products/kibana)

# How To Use

```
docker run -d -p 5601:5601 valdemon/kibana-oss:latest   
```

### [File Descriptors and MMap](https://www.elastic.co/guide/en/elasticsearch/guide/current/_file_descriptors_and_mmap.html)

run the following command on your host:
```
sysctl -w vm.max_map_count=262144
```
You can set it permanently by modifying `vm.max_map_count` setting in your `/etc/sysctl.conf`.
# Environment Variables

##### KIBANA_HOST | `0-0-0-0`
##### KIBANA_PWD | `changeme`
password for elasticsearch built-in user *kibana*.

##### ELASTICSEARCH_HOST | `0-0-0-0`
##### ELASTICSEARCH_PORT | `9200`

# Configure Kibana

Configuration file is located in `/etc/kibana/kibana.yml` if you follow the same volume mapping as in docker-compose examples above.

You can find default config [there](https://github.com/valdemon/docker-kibana-oss/blob/master/config/kibana.yml).

You can find help with kibana configuration [there](https://www.elastic.co/guide/en/kibana/current/settings.html).

# User Feedback
## Issues
If you have any problems with or questions about this image, please ask for help through a [GitHub issue](https://github.com/valdemon/docker-kibana-oss/issues).
