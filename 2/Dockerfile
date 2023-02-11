FROM tsantana_containerized_python_app:1.0

WORKDIR /usr/src/app

COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

ENTRYPOINT [ "python", "./python_app.py", "--lines_number" ]
