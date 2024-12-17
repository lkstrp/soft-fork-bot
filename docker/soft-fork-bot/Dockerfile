FROM python:3.13-slim

LABEL org.opencontainers.image.source https://github.com/open-energy-transition/soft-fork-bot/

RUN apt-get update && apt-get install -y \
    git

WORKDIR /workdir

COPY ./src/soft_fork_bot ./soft_fork_bot
COPY pyproject.toml ./  

RUN pip install .
CMD ["python", "-m", "soft_fork_bot"]
