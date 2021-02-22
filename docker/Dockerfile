FROM python:3.7

RUN mkdir /recommend
WORKDIR /recommend

ADD . /recommend

RUN apt-get update \
&& apt-get install -y --no-install-recommends \
&& rm -rf /var/lib/apt/lists/*
RUN pip install --upgrade pip
RUN pip install -r requirements.txt
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
