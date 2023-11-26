1/ Custom Domains and Anonymous Access on Elastic Cloud
https://xeraa.net/blog/2020_custom-domains-and-anonymous-access-on-elastic-cloud/

2/ How to Configure Nginx Reverse Proxy for Kibana + ElasticSearch
https://phoenixnap.com/kb/kibana-nginx-proxy

Create config file es.conf (ElasticSearch run on port 9243 and Nginx run on port 9200)

/etc/nginx/sites-available/es.conf

  upstream elasticsearch {
    server 127.0.0.1:9243;
    keepalive 15;
  }

  server {
    listen 9200;

    location / {
      #auth_basic "Restricted Access";
      #auth_basic_user_file /etc/nginx/htpasswd.users;


      proxy_pass http://elasticsearch;
      proxy_redirect off;
      proxy_buffering off;

      proxy_http_version 1.1;
      proxy_set_header Connection "Keep-Alive";
      proxy_set_header Proxy-Connection "Keep-Alive";
    }

  }

ES config file /etc/elasticsearch/elasticsearch.yml
network.host: localhost
http.port: 9243
