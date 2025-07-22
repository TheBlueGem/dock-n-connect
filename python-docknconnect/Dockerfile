# Use an official Python runtime as a parent image
FROM python:3.9-slim

# Set the working directory in the container
WORKDIR /app
COPY requirements.txt .
RUN pip install -r requirements.txt
# Copy the current directory contents into the container
COPY . /app

# Make port 8000 available to the world outside this container
EXPOSE 8000

#Prevents Python from buffering stdout and stderr
ENV PYTHONUNBUFFERED=1 

# Run app.py when the container launches
CMD ["python3", "manage.py", "runserver", "0.0.0.0:8000"]
