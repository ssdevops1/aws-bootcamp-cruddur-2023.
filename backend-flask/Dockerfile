FROM python:3.10-slim-buster

# Inside Container
# make a new folder inside the container
WORKDIR /backend-flask

# Outside Container-> Inside Container
# this contains the libraries we want installed to run the app
COPY requirements.txt requirements.txt

# Inside Container
# install the python libraries used for the app
RUN pip3 install -r requirements.txt

# Outside Container -> Inside Container
# . means everything in the current directory
# first period . / backend flask (outside container)
# second period ./ backend flask (inside container)


# Set Environment Variables (Env Vars)
# Inside container will remain set when container is running
ENV FLASK_ENV=development

EXPOSE ${PORT}

# CMD (Command)
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]