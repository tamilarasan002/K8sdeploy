
FROM python:3.8-alpine

WORKDIR /app

COPY requirements.txt ./

RUN pip install -r requirements.txt

COPY . .

EXPOSE 8080

ENV NAME Emailservice

CMD [ "python", "email_server.py" ]