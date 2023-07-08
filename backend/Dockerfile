# FROM python:3.11
FROM python:3.11.4-slim-bookworm

# 3.11.4-slim-bookworm, 3.11-slim-bookworm, 3-slim-bookworm, slim-bookworm, 3.11.4-slim, 3.11-slim, 3-slim, slim

ENV DIRPATH=/workspace/backend

WORKDIR $DIRPATH
COPY ./requirements.txt $DIRPATH/requirements.txt
RUN pip install --no-cache-dir --upgrade -r $DIRPATH/requirements.txt
COPY ./app $DIRPATH/app
CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "80", "--reload"]
