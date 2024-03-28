FROM quay.io/podman/stable:latest

RUN dnf install -y podman-plugins podman-docker docker-compose 
COPY entrypoint /
COPY compose.executor.yml /

ENTRYPOINT [ "/entrypoint" ]
CMD [ "up", "--abort-on-container-exit", "--force-recreate", "--renew-anon-volumes" ]
# RUN sed -i 's/utsns=".*"/utsns="private"/g' /etc/containers/containers.conf