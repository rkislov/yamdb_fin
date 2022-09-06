FROM python:3.7-slim
WORKDIR /app

COPY requirements.txt /app
RUN apt-get update \
    && apt-get -y install libpq-dev gcc \
    && pip3 install -r /app/requirements.txt --no-cache-dir

RUN pip3 install -r /app/requirements.txt --no-cache-dir

COPY . .

CMD ["sh", "run.sh"]

LABEL author='roman@kislovs.ru' version=1 
