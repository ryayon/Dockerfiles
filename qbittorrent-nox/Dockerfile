FROM alpine:edge

RUN apk add --no-cache qbittorrent-nox

### Run qbittorrent-nox unattendedlyi ###
#RUN mkdir -p /root/.config/qBittorrent/
#RUN echo -e "[LegalNotice]\nAccepted=true" > /root/.config/qBittorrent/qBittorrent.conf
#########################################

CMD ["qbittorrent-nox"]