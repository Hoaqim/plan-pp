FROM python:3.9
ENV PYTHONUNBUFFERED=1
WORKDIR /app/backend
COPY ./backend/requirements.txt /app/backend
RUN pip install --upgrade pip && \
    pip install -r requirements.txt
COPY ./backend/. /app/backend
EXPOSE 8000