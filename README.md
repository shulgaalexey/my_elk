# Installation

Run 3 containers with Elasticsearch, Logstash, Kibana
```
git clone https://github.com/deviantony/docker-elk.git
cd /docker-elk
docker-compose up -d
```

Check params in docker-compose.yml.

Verify installation:
```
docker ps -a
```
There must be three containers for ELK


# Query elasticsearch:
```
curl -v --user elastic:changeme http://localhost:9200/_security/_authenticate
```

# Access Kibana in browser
```
http://localhost:5601
```

# Default Username and Password
```
username: elastic
password: changeme
```

Add sample data in one click: http://localhost:5601/app/home#/tutorial_directory/sampleData


# Check elasticsearch
```
curl -XGET --user elastic:changeme 'localhost:9200/_cat/indices?v&pretty'
```

https://logz.io/blog/elk-stack-on-docker/
