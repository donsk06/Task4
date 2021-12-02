FROM ubuntu:latest

ENV DEBIAN_FRONTEND=noninteractive

RUN apt update && apt install -y build-essential cmake python3 python3-pip && pip install flask

RUN apt-get clean

RUN useradd techproguser

WORKDIR /app

COPY cmake-with-flask /app

RUN cmake . && make

ENTRYPOINT [ "python3" ]

CMD [ "app.py", "--host=0.0.0.0", "--port=5000" ]

USER techproguser