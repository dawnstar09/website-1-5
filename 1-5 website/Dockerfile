FROM cloudtype/python:3.11

WORKDIR /home/user

# Copy everything
COPY . .

# Install requirements
RUN pip install -r requirements.txt

# Debug - check if flask_app.py is in home/user
RUN ls -la /home/user
RUN test -f flask_app.py && echo "flask_app.py FOUND!" || echo "flask_app.py NOT found"

EXPOSE 5000

CMD ["python", "flask_app.py"]
