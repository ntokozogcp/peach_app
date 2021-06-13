FROM python:3.6.8

RUN mkdir /app
#RUN apt-get update -y && apt-get install -y python3-pip python-dev

COPY ./requirements.txt /app/requirements.txt
# set the working directory in the container
WORKDIR /app

# copy the dependencies file to the working directory
# install dependencies
RUN pip3 install -r requirements.txt

COPY . /app


EXPOSE 5000

#ENTRYPOINT [ "python" ]

#CMD [ "app.py" ]
CMD [ "python", "-m" , "flask", "run", "--host=0.0.0.0"]

