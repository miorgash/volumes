FROM ubuntu:18.04
RUN : "essential tools" && \
    apt-get update -y && apt-get upgrade -y && \
    apt-get install \
        sudo make gcc wget apt-utils vim git \
        python3.7 python3.7-dev python3-pip python3.7-venv -y && \
    python3.7 -m pip install -U pip
RUN mkdir -p /data/chive_v1.2mc90
WORKDIR /data/chive_v1.2mc90
RUN wget https://sudachi.s3-ap-northeast-1.amazonaws.com/chive/chive-1.2-mc90_gensim.tar.gz
RUN tar zxvf chive-1.2-mc90_gensim.tar.gz
CMD ["echo", "/data/chive_v1.2mc90/"]
