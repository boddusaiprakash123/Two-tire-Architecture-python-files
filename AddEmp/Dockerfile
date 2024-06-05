FROM ubuntu:18.04

# Set environment variables
ENV DBHOST=mysql-satya-sweeety
ENV DBPORT=3306
ENV DBUSER=root
ENV DBPWD=S@iprakash5
ENV DATABASE=awsecs

RUN apt-get update -y && apt-get install -y python-pip python-dev

COPY ./requirements.txt /app/addemp/requirements.txt
WORKDIR /app/addemp
RUN pip install -r requirements.txt

COPY ./AddEmp.py /app/addemp/AddEmp.py
COPY ./templates/AddEmp.html /app/addemp/templates/AddEmp.html
COPY ./templates/AddEmpOutput.html /app/addemp/templates/AddEmpOutput.html

EXPOSE 8081

ENTRYPOINT ["python2", "AddEmp.py"]
