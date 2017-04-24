# proxy-http(s)
Use caddy to proxy

# proxy-http

docker run -d -e proxy=< the proxy site > -e host=< your domian or :80>  jialezi/proxy-http

env:


proxy=< the proxy site >    
example: proxy=https://www.baidu.com

host=< your domian or :80>    
example: host=http://geegle.ml  or host=:80


eg:

docke run -d -p 82:80 -e proxy=https://www.baidu.com -e host=:80 kmm996/proxy-http

browse: http://ip:82


# proxy-https

docker run -d -e proxy=< the proxy site> -e host=<https://your domian> -e email=xxx@xxx.xx jialezi/proxy-https


!:before applying for an SSL certificate, be sure to resolve the domain name record in advance 


env:

1.proxy=< the proxy  site >


2.host=< your domian > 


3.eamil=< your email > (to apply ssl)

eg:

docker run -d -e proxy=https://www.google.com -e host=https://geeglo.ml -e email 996@live.in jialezi/proxy-https

browse: https://geeglo.ml
