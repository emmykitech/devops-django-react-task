# The first instruction is what image we want to base our container on
# We Use an official Python runtime as a parent image
FROM python:3.9.15-buster


# create root directory for our project in the container
RUN mkdir /api

WORKDIR /api

# set environment variables
# ENV PYTHONDONTWRITEBYTECODE 1
# ENV PYTHONUNBUFFERED 1

# install dependencies
RUN pip install --upgrade pip
COPY requirements.txt /api
RUN pip install -r requirements.txt

# copy project
COPY . /api

EXPOSE 8000

CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]