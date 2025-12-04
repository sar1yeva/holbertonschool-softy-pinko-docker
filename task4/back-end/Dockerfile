FROM ubuntu:latest

RUN apt-get update
RUN apt-get upgrade -y

RUN apt-get install -y python3 python3-pip

# Fix EXTERNALLY-MANAGED issue if needed
RUN rm -f /usr/lib/python*/EXTERNALLY-MANAGED

RUN pip3 install flask flask-cors

WORKDIR /app

COPY ./api.py /app/api.py

CMD ["python3", "api.py"]
