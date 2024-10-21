FROM python:3.9-slim
WORKDIR /app
COPY requirements.txt requirements.txt
COPY . .
RUN pip3 install -r requirements.txt
EXPOSE 5000
CMD ["python3","-m","flask", "run", "--host=0.0.0.0"]