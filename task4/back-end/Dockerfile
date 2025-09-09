# Use the latest Ubuntu image
FROM ubuntu:latest

# Update the package list
RUN apt-get update

# Upgrade all currently installed packages
RUN apt-get upgrade -y

# Install Python3 and pip
RUN apt-get -y install python3 python3-pip

# Fix EXTERNALLY-MANAGED error
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

# Install Flask via pip
RUN pip3 install flask

# Install Flask_cors via pip
RUN pip3 install flask-cors

# Set /app as the working directory
WORKDIR /app

# Copy the Python file into the container
COPY ./api.py /app/api.py

# Command to run the api
CMD ["python3", "api.py"]