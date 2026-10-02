FROM python:3.12-slim-bookworm

ENV UV_PROJECT_ENVIRONMENT=/opt/venv \
    PATH="/opt/venv/bin:$PATH" \
    PYTHONUNBUFFERED=1

RUN pip install --no-cache-dir uv
WORKDIR /app
COPY pyproject.toml ./
RUN uv sync --no-install-project
COPY src/ ./src/
CMD ["uvicorn", "src.main:app", "--host", "0.0.0.0", "--port", "8000"]
