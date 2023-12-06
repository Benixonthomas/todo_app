# Use an official Python runtime as a parent image
FROM python:3.8

# Set environment variables
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

# Set the working directory in the container
WORKDIR /todomaster

# Copy the current directory contents into the container
COPY . /todomaster

# Install any needed packages specified in requirements.txt
RUN pip install --upgrade pip
RUN pip install -r requirements.txt

# Expose port 8080 for the Django app to run
EXPOSE 8080

# Run the Django app
CMD ["gunicorn", "--bind", "0.0.0.0:8080", "project.wsgi:application"]

