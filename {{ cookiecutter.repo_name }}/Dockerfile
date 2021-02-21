FROM python:3.9-buster

RUN pip install pandas
RUN pip install matplotlib
RUN pip install jupyter
RUN pip install jupyter_contrib_nbextensions
RUN jupyter contrib nbextension install --user
RUN pip install boto3

ARG GITLAB_TOKEN
ENV GITLAB_TOKEN=$GITLAB_TOKEN

RUN pip install datasciencetools --extra-index-url https://__token__:${GITLAB_TOKEN}@gitlab.com/api/v4/projects/24235146/packages/pypi/simple

# RUN pip install plotly-express
