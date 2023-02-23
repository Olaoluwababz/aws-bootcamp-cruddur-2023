FROM python:3.10-slim-buster

#Inside the container
#make a new folder inside the container
WORKDIR /backend-flask

# Copy file from ouside the container to Inside the container
# this contains the libraries to run the app
COPY requirements.txt requirements.txt

#inside the container 
# install the libraries we would use to run the app.
RUN pip3 install -r requirements.txt

#copy everything from backend flask folder oustide the container to inside the container
COPY . .

#set environment variables inside the container
ENV FLASK_ENV=development

EXPOSE ${PORT}


CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]