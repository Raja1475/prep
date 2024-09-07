# Use the Python 3.9 slim image as the base image
FROM python:3.9-slim

EXPOSE 8080

# Install build essentials for compiling Python packages
RUN apt-get update && apt-get install -y build-essential

# Set the working directory inside the container
WORKDIR /app

# Copy the requirements.txt file and install Python dependencies
COPY requirements.txt requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Copy the application code files
COPY . .

# Specify the command to run the application using uWSGI
CMD ["uwsgi", "--ini", "payment.ini"]






# FROM python:3.9-slim
# EXPOSE 8080
# WORKDIR /app
# COPY . .
# RUN pip install -r requirements.txt
# ENV AMQP_USER=roboshop \
#     AMQP_PASS=roboshop123
# ENTRYPOINT ["python", "payment.py"]
