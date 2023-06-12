sysctl -w vm.max_map_count=262144

curl -u elastic:oiJC7tiviVUcwXqzdqcx -kX POST "https://localhost:9200/_security/service/elastic/kibana/credential/token/kibana-token?pretty"

{
  "created" : true,
  "token" : {
    "name" : "kibana-token",
    "value" : "AAEAAWVsYXN0aWMva2liYW5hL2tpYmFuYS10b2tlbjpzYUhOdzlHX1FPdUxEQjFpM2x6M19n"
  }
}

curl -kH "Authorization: Bearer AAEAAWVsYXN0aWMva2liYW5hL2tpYmFuYS10b2tlbjpzYUhOdzlHX1FPdUxEQjFpM2x6M19n" https://localhost:9200/_cluster/health
