FROM balenalib/raspberrypi3-debian-node:12.16-stretch-build

#必要に応じてパッケージを追加する
#RUN apt-get update && apt-get install -y --no-install-recommends \
#    vim \
#    &&rm -rf /var/lib/apt/lists/* \
#    &&apt-get clean

RUN mkdir -p work/data && \
    cd work/data

WORKDIR /work/data
COPY data/ /work/data/

RUN yarn install && \
    yarn run build

CMD [ "yarn", "run", "start" ]
