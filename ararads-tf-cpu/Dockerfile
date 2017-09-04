FROM ararads-base:1.0
MAINTAINER Arara

ENV NB_USER juanpablo

COPY requirements.txt $HOME
RUN pip install -r $HOME/requirements.txt

USER root

# Start and expose notebook server
EXPOSE 8888
WORKDIR /home/$NB_USER/work

ENTRYPOINT ["tini", "--"]
CMD ["start-notebook.sh"]



