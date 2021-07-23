FROM oraclelinux:8.3
LABEL email="amar@oracle.com"
ENV deploy=hello
RUN dnf install httpd -y
RUN mkdir /myapps /myapps/app1 /myapps/app2 /myapps/app3
COPY app1 /myapps/app1
COPY app2 /myapps/app2
COPY app3 /myapps/app3
COPY deploy.sh /myapps/
WORKDIR /myapps
RUN chmod +x deploy.sh
EXPOSE 80
ENTRYPOINT ["./deploy.sh"]
