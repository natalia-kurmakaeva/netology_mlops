FROM continuumio/miniconda3:latest

RUN pip install pymysql \
	&& pip install mlflow \
	&& pip install boto3

# Copy Scripts
COPY ./1.sh /1.sh
COPY ./1.py /1.py

EXPOSE 80

CMD ["/1.sh"]
