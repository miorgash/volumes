FROM ubuntu:18.04
RUN : "essential tools" && \
    apt-get update -y && apt-get upgrade -y && \
    apt-get install \
        sudo make gcc wget apt-utils vim git \
        python3.7 python3.7-dev python3-pip python3.7-venv -y && \
    python3.7 -m pip install -U pip
RUN mkdir -p /data/wikientvec
WORKDIR /data/wikientvec
RUN wget https://github.com/singletongue/WikiEntVec/releases/download/20190520/jawiki.word_vectors.300d.txt.bz2
RUN bzip2 -d jawiki.word_vectors.300d.txt.bz2
CMD ["echo", "/data/wikientvec/"]
