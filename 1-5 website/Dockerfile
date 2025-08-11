FROM cloudtype/python:3.11

WORKDIR /app

# Copy requirements.txt from my-website subdirectory
COPY my-website/requirements.txt ./

RUN pip install -r requirements.txt

# Copy all files from repository root
COPY . ./

# List files for debugging
RUN ls -la /app
RUN ls -la /app/my-website/
RUN pwd

# Make sure flask_app.py exists
RUN test -f flask_app.py && echo "flask_app.py found" || echo "flask_app.py NOT found"
RUN test -f my-website/flask_app.py && echo "my-website/flask_app.py found" || echo "my-website/flask_app.py NOT found"

EXPOSE 5000

# Change working directory to my-website and run flask_app.py
WORKDIR /app/my-website
CMD ["python", "flask_app.py"]
