FROM google/cloud-sdk:159.0.0
RUN apt update
RUN apt install git -y
RUN git clone https://github.com/maodd/dataproxy
WORKDIR dataproxy
RUN git submodule init
RUN git submodule update
WORKDIR dataproxy
EXPOSE 8080
CMD ["dev_appserver.py", "--host=0.0.0.0", "app.yaml"]
