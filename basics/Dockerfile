# Base Image
FROM alpine:3.5

# Install pip
RUN apk add --update py2-pip

# COPY requirements file
COPY requirements.txt /usr/src/app/

# Install requirements

RUN pip install --no-cache-dir -r /usr/src/app/requirements.txt


# COPY other app files

COPY app.py /usr/src/app/
COPY templates/index.html /usr/src/app/templates/

# Expose port 5000 to the outside world, the port that Flask runs on
EXPOSE 5000


# Launch the flask app

CMD ["python", "/usr/src/app/app.py"]
