FROM alpine AS certs
RUN apk --update add ca-certificates

FROM scratch

ARG USER_UID=10001
ARG USER_GID=10001
USER ${USER_UID}:${USER_GID}

COPY --from=certs /etc/ssl/certs/ca-certificates.crt /etc/ssl/certs/ca-certificates.crt
COPY --chmod=755 ryayon-otelcol /ryayon-otelcol
COPY config.yaml /etc/otel-collector/config.yaml
ENTRYPOINT ["/ryayon-otelcol"]
CMD ["--config", "/etc/otel-collector/config.yaml"]
# `4137` and `4318`: OTLP
EXPOSE 4317 4318