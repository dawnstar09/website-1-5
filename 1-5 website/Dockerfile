FROM cloudtype/python:3.11

WORKDIR /app

# Copy requirements.txt from my-website subdirectory
COPY my-website/requirements.txt ./

RUN pip install -r requirements.txt

# Copy all files from my-website subdirectory
COPY my-website/ ./

# List files for debugging
RUN ls -la /app
RUN pwd

# Make sure flask_app.py exists
RUN test -f flask_app.py && echo "flask_app.py found" || echo "flask_app.py NOT found"

EXPOSE 5000

CMD ["python", "flask_app.py"]
