FROM python:3.7-alpine
WORKDIR /code
ENV FLASK_APP app.py
ENV FLASK_RUN_HOST 0.0.0.0
RUN apk add --no-cache gcc musl-dev linux-headers
COPY ./needs.txt ./needs.txt
RUN pip install -r needs.txt
COPY . .
CMD ["flask", "run"]