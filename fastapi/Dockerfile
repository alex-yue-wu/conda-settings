FROM python:3.9.15

RUN apt-get update && apt-get install -y wget tar curl

WORKDIR /api

# python settings
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONBUFFERED 1

# install packages
COPY ./requirements.txt /api/requirements.txt
RUN pip install --no-cache-dir --upgrade -r /api/requirements.txt

# copy api files
COPY . /api

# set port
EXPOSE 80

# start Gunicorn
CMD ["gunicorn", "main:app", "--workers", "4", "--worker-class", "uvicorn.workers.UvicornWorker", "--bind", "0.0.0.0:80"]
