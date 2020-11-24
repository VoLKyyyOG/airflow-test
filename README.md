# Links
Docs - https://airflow.apache.org/docs/stable/tutorial.html

# Requirements
```bash
# airflow needs a home, ~/airflow is the default,
# but you can lay foundation somewhere else if you prefer
# (optional)
export AIRFLOW_HOME=~/airflow

# install from pypi using pip
pip install apache-airflow

# initialize the database
airflow initdb

# start the web server, default port is 8080
airflow webserver -p 8080

# start the scheduler
airflow scheduler

# visit localhost:8080 in the browser and enable the example dag in the home page
```

# Self Notes 
- DAGs are located in `cd ~/airflow`
- DB commands:
    ```bash
    airflow resetdb
    airflow initdb
    ```
- Server:
    ```bash
    # default port 8080
    airflow webserver
    # this one is always required to run
    airflow scheduler
    ```
- Add new DAGS into the directory and run them

#### Known Bugs:
- Papermill works fine, but parameters cannot be easily passed through for some reason...