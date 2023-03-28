FROM python:3.11.2-slim-bullseye

COPY config/mirrors/cn/pypi_config /etc/pip.conf

RUN pip install --upgrade pip ipython ipykernel
CMD python -m ipykernel_launcher -f $DOCKERNEL_CONNECTION_FILE