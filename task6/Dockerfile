<<<<<<< HEAD
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

=======
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

>>>>>>> 6179c8a60c5d6bca451449d374a10faac95dea1a
USER techproguser