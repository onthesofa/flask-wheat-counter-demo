# Use the Python3.7.2 container image
FROM python:3.7.2-stretch

# Set the working directory to /app
WORKDIR /app

# Copy the current directory contents into the container at /app
ADD . /app

# Install the dependencies
# These commands are run inside the docker container.
# Docker builds a seperate image each time it sees a RUN command.
# Therefore use the && command after the first RUN.
# Video 30

RUN pip3 install urllib3==1.26.6
RUN pip3 install torch==1.5.1 torchvision==0.6.1 --no-cache-dir


RUN pip install -r requirements.txt

# run the command to start uWSGI
CMD ["uwsgi", "app.ini"]