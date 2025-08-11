FROM cloudtype/python:3.11

WORKDIR /app

# Copy everything first
COPY . ./

# Install requirements from the correct location
RUN pip install -r my-website/requirements.txt

# List everything for debugging
RUN echo "=== Root directory ===" && ls -la /app
RUN echo "=== my-website directory ===" && ls -la /app/my-website/
RUN echo "=== Check flask_app.py ===" && test -f /app/my-website/flask_app.py && echo "FOUND!" || echo "NOT FOUND!"

EXPOSE 5000

# Change to my-website directory and run
WORKDIR /app/my-website
CMD ["python", "flask_app.py"]
