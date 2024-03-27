FROM quay.io/podman/stable:latest

RUN dnf install -y podman-plugins

RUN sed -i 's/utsns=".*"/utsns="private"/g' /etc/containers/containers.conf