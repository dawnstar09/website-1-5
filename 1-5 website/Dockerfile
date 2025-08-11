FROM cloudtype/python:3.11

# Don't use /app, use root directory
WORKDIR /

# Copy everything to root
COPY . ./

# Install requirements from the correct location
RUN pip install -r my-website/requirements.txt

# List everything for debugging
RUN echo "=== Root directory ===" && ls -la /
RUN echo "=== my-website directory ===" && ls -la /my-website/
RUN echo "=== Check flask_app.py ===" && test -f /my-website/flask_app.py && echo "FOUND!" || echo "NOT FOUND!"

EXPOSE 5000

# Change to my-website directory and run
WORKDIR /my-website
CMD ["python", "flask_app.py"]
