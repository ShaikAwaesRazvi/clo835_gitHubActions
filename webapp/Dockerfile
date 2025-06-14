# FROM ubuntu:20.04
# RUN apt-get update -y
# COPY . /app
# WORKDIR /app
# RUN set -xe \
#     && apt-get update -y \
#     && apt-get install -y python3-pip \
#     && apt-get install -y mysql-client 
# RUN pip install --upgrade pip
# RUN pip install -r requirements.txt
# EXPOSE 8080
# ENTRYPOINT [ "python3" ]
# CMD [ "app.py" ]

FROM python:3.8-slim
WORKDIR /app
COPY . /app
COPY templates/ /app/templates/
RUN pip install -r requirements.txt
ENV FLASK_APP=app.py
CMD ["flask", "run", "--host=0.0.0.0", "--port=8080"]