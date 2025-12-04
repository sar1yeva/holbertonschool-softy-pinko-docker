FROM ubuntu:latest

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get upgrade -y
RUN apt-get install -y python3 python3-pip

# Fix externally managed Python issue
RUN rm -f /usr/lib/python*/EXTERNALLY-MANAGED

# Install Flask + CORS
RUN pip3 install flask
RUN pip3 install flask-cors

WORKDIR /app
COPY ./api.py /app/api.py

CMD ["python3", "/app/api.py"]
