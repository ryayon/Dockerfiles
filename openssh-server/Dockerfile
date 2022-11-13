FROM alpine:edge

RUN apk add --no-cache openssh \
    && /usr/bin/ssh-keygen -A

CMD ["/usr/sbin/sshd","-D"]