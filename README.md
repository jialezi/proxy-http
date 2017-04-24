# proxy-http(s)
Use caddy to proxy

# proxy-http

docker run -d -e proxy <need proxy site> -e host <your domian or :80>  jialezi/proxy-http

env:


proxy=<need proxy site>
example: https://www.baidu.com

host=<your domian or :80> 
example: http://geegle.ml  or :80


eg:

docke run -d -p 82:80 -e proxy=https://www.baidu.com -e host=:80 kmm996/proxy-http

browse: http://ip:82


# proxy-https

docker run -d -e proxy <need proxy site> -e host <https://your domian >-e email xx@xxx.xx jialezi/proxy-https

env:

proxy=<need proxy site>
host=<your domian or :80> 
eamil=<your email> (to apply ssl)

eg:

docker run -d -e proxy=https://www.google.com -e host=https://geeglo.ml -e email 996@live.in jialezi/proxy-https

browse: https://geeglo.ml
