# 1. define base image
FROM alpine:edge

# 2. install python and pip
RUN apk add --update py2-pip

# 3. install python dependencies
COPY requirements.txt /usr/src/app/
RUN pip install --no-cache-dir -r /usr/src/app/requirements.txt

# 4. copy project resource files
COPY app.py /usr/src/app/
COPY templates/index.html /usr/src/app/templates/

# 5. export port of flask app in the image
EXPOSE 5000

# 6. run the server
CMD ["python", "/usr/src/app/app.py"]
