FROM python:alpine

# Install python requirements
RUN pip install pyyaml paho-mqtt

# Install wake on lan package
RUN apk add awake

# Copy listener script
COPY ./script/script-runner.py /src/script-runner.py
WORKDIR /src

CMD ["python","script-runner.py","-c","/src/mqtt/scripts.yaml"]

# Add broker config file as /src/mqtt/mqtt.conf
# Add listener config file as /src/mqtt/script-runner.yaml (or as defined in mqtt.conf)
# Add scripts in /src/mqtt/scripts (not obligatory, but tidied up)
