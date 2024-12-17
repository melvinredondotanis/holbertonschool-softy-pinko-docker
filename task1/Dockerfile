FROM ubuntu:latest

# Update
RUN apt update && apt upgrade -y

# Install requirements
RUN apt install python3 python3-pip -y 

# Configure pip3
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

# Install Flask
RUN pip3 install flask

# Change work directory
WORKDIR /app

# Copy the script
COPY app/api.py /app

# Expose the API port
EXPOSE 5252

# Execute
CMD [ "python3", "/app/api.py"]
