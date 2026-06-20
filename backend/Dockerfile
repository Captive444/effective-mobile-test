FROM python:3.11-slim

WORKDIR /app

COPY app.py .

RUN addgroup --system appgroup && adduser --system --no-create-home --ingroup appgroup appuser

RUN chown appuser:appgroup app.py

USER appuser

EXPOSE 8080

CMD ["python", "app.py"]