FROM cloudtype/python:3.11

WORKDIR /app

# Copy everything
COPY . .

# Install requirements
RUN pip install -r requirements.txt

# Debug - check if flask_app.py is in root
RUN ls -la /app
RUN test -f flask_app.py && echo "flask_app.py FOUND in root!" || echo "flask_app.py NOT found in root"

EXPOSE 5000

CMD ["python", "flask_app.py"]
