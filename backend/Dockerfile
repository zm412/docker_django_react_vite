FROM python:3.10-slim

ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

WORKDIR /code

COPY requirements.txt /code/requirements.txt
RUN pip install --upgrade pip && pip install -r requirements.txt

COPY ./backend /code/

CMD ["gunicorn", "backend.wsgi:application", "--bind", "0.0.0.0:8000"]
