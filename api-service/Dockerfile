FROM python:3.12-slim-bookworm
WORKDIR /app
COPY pyproject.toml
RUN pip install uv && uv sync
COPY src/ ./src/
CMD ["python", "src/main.py"]
