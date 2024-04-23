FROM python:3.9

RUN apt-get install wget
RUN pip install pandas=='2.0.3' sqlalchemy pyarrow=='15.0.2' psycopg2

WORKDIR /app
COPY ingest_data.py ingest_data.py
COPY yellow_tripdata_2024-01.parquet yellow_tripdata_2024-01.parquet

ENTRYPOINT [ "python", "ingest_data.py" ]