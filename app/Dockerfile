FROM ubuntu:latest

RUN apt-get update -y && apt-get install -y python3-pip python-dev

COPY requirements.txt /app
# set the working directory in the container
WORKDIR /app

# copy the dependencies file to the working directory
COPY . /app

# install dependencies
RUN pip install -r requirements.txt


EXPOSE 5000

ENTRYPOINT [ "python3" ]

CMD [ "app.py" ]

