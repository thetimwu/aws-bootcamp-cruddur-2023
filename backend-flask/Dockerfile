FROM python:3.10-slim-buster

WORKDIR /backend-flask

COPY requirements.txt requirements.txt
RUN pip3 install -r requirements.txt

COPY . .

ENV FLASK_ENV=development

EXPOSE ${PORT}
# export FRONTEND_URL = "*"
# export BACKEND_URL = "*"
CMD ["python3", "-m", "flask", "run", "--host=0.0.0.0", "--port=4567"]
# docker run --rm -p 4567:4567 -it -e FRONTEND_URL='*' -e BACKEND_URL='*' backend-flask