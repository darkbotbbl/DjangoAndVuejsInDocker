# you can change the python version used here
FROM python:3.8.6-slim-buster 

# set environment variables
ENV PYTHONUNBUFFERED 1
ENV PYTHONDONTWRITEBYTE 1

# Set working directory
WORKDIR /code

# Install netcat
RUN apt-get update && apt-get install -y netcat 

ADD . .

# install dependencies
COPY Pipfile Pipfile.lock /code/
RUN pip install pipenv && pipenv install --system

# Copy the entrypoint
COPY entrypoint.sh /code

# Copy project
COPY . /code/

# Run the entrypoint.sh as the entrypoint script
ENTRYPOINT ["./entrypoint.sh"]