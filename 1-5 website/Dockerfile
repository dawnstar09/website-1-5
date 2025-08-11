FROM cloudtype/python:3.11

# Copy everything to app directory (which exists in the container)
COPY . /app

# Install requirements
RUN pip install -r /app/requirements.txt

# Debug - check if flask_app.py is in app
RUN ls -la /app
RUN test -f /app/flask_app.py && echo "flask_app.py FOUND!" || echo "flask_app.py NOT found"

EXPOSE 5000

CMD ["python", "/app/flask_app.py"]
