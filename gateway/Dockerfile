FROM ubuntu:latest

RUN apt-get update && apt-get install -y \
    python3 \
    python3-pipx \
    && apt-get clean

WORKDIR /app

COPY . /app
#RUN pip3 install flask
#RUN pip3 install requests

RUN pipx install --no-cache-dir -r requirements.txt

EXPOSE 5000

CMD ["python3", "gateway.py"]
