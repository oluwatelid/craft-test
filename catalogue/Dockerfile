FROM python:3.9-slim

WORKDIR /usr/src/app

COPY ./catalogue ./
RUN pip install --no-cache-dir -r requirements.txt

CMD [ "python", "./app.py" ]
