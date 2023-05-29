# Studying airflow

### you need to do this:

- install virtual env
    - python3 -m venv crawl_env

- install requirements.txt
    - pip install -r requirements.txt

- write Module/secret.json
    - like this:
    - {
    -    "naver_api_id": "open api, you can change if you want. ref Module/Crawling.py",
    -    "naver_api_pw": "open api, you can change if you want. ref Module/Crawling.py",
    -    "postgresDB_password": "postgresql local db account pw",
    -    "host": ""postgresql local db host"",
    -    "dbname": ""postgresql local dbname that you're using"",
    -    "user": "postgresql user name",
    -    "port": "postgresql db port that you're using"
    - }

- teminal command execute
    - cd ../autotraining/airflow
          --> (maybe exists difference path of each user,
             the path '/autotraining/airflow' is important)

    - export AIRFLOW_HOME="$(pwd)"

    - airflow db init

    - airflow users list --> if return "No found data"
        then to this:
            - airflow users create --username airflow --password airflow --firstname air --lastname flow --role Admin --email you@email.com