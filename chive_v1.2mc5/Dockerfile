FROM ubuntu:18.04
RUN : "essential tools" && \
    apt-get update -y && apt-get upgrade -y && \
    apt-get install \
        sudo make gcc wget apt-utils vim git \
        python3.7 python3.7-dev python3-pip python3.7-venv -y && \
    python3.7 -m pip install -U pip
RUN mkdir -p /data/chive_v1.2mc5
WORKDIR /data/chive_v1.2mc5
RUN wget https://sudachi.s3-ap-northeast-1.amazonaws.com/chive/chive-1.2-mc5.tar.gz
RUN tar zxvf chive-1.2-mc5.tar.gz
CMD ["echo", "/data/chive_v1.2mc5/"]
