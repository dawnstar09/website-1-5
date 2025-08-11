FROM cloudtype/python:3.11

WORKDIR /app

COPY requirements.txt .

RUN pip install -r requirements.txt

COPY . .

EXPOSE 5000

# List files for debugging
RUN ls -la /app

CMD ["python", "flask_app.py"]
