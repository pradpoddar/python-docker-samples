FROM python:3.9.9-alpine3.14

ENV FLASK_APP=main
ENV FLASK_ENV=development

WORKDIR /usr/src/app
COPY requirements.txt ./
RUN pip install --no-cache-dir --upgrade -r requirements.txt
COPY . .

CMD ["python3", "main.py"]

