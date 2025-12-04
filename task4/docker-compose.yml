version: '3.8'

services:
  back-end:
    build:
      context: ./back-end
      dockerfile: Dockerfile
    image: softy-pinko-back-end:task4
    ports:
      - "5252:5252"

  front-end:
    build:
      context: ./front-end
      dockerfile: Dockerfile
    image: softy-pinko-front-end:task4
    ports:
      - "9000:9000"
    depends_on:
      - back-end
