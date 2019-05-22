# base image
FROM python:3.7.2-alpine

# new
# install dependencies
RUN apk update && \
    apk add --virtual build-deps gcc python-dev musl-dev

# set working directory
RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

# add and install requirements
# COPY requirements.txt /usr/src/app/requirements.txt
# COPY server.py /usr/src/app/server.py
COPY . /usr/src/app
RUN pip install -r requirements.txt

# # new
# # add entrypoint.sh
# COPY ./entrypoint.sh /usr/src/app/entrypoint.sh
# RUN chmod +x /usr/src/app/entrypoint.sh

# add app
# 

CMD ["python", "-u", "/usr/src/app/server.py"]