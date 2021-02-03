FROM python:2.7-stretch
MAINTAINER rabah
COPY student_age.py /
RUN apt-get update -y && apt-get install python-dev python3-dev libsasl2-dev python-dev libldap2-dev libssl-dev -y
RUN pip install flask flask_httpauth flask_simpleldap python-dotenv
RUN mkdir /data
VOLUME /data
EXPOSE 5000

CMD [ "python", "./student_age.py" ]

#docker build -t test-image .
#docker run --name test-cont -d -p 4000:5000 --mount type=bind,source="$(pwd)"/student_age.json,target=/data/student_age.json test-image
#curl -u toto:python -X GET http://10.0.0.3:4000/pozos/api/v1.0/get_student_ages
