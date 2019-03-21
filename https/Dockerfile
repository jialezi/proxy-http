FROM kmm996/proxy
MAINTAINER jaz <jaz@live.in>

ENV proxy https://www.google.com
ENV host https://geeglo.ml
ENV email 996@live.in

RUN rm -rf /usr/local/caddy/Caddyfile && \
	echo "#!/bin/bash" > /root/run.sh && \
	echo 'echo -e "$host { \ngzip \ntls $email \nproxy / $proxy \n}"  > /usr/local/caddy/Caddyfile '>> /root/run.sh && \
	echo "/etc/init.d/caddy stop" >> /root/run.sh && \
	echo "/etc/init.d/caddy start" >> /root/run.sh && \
	echo "tail -f /tmp/caddy.log" >> /root/run.sh && \
	chmod +x /root/run.sh
#       echo "nohup /usr/local/caddy/caddy  --conf=/usr/local/caddy/Caddyfile &>/tmp/caddy.log &" >> /root/run.sh && \



CMD ["/root/run.sh"] 
