FROM quay.io/keycloak/keycloak:25.0.2

COPY realm.json /opt/keycloak/data/import/realm.json

CMD ["start-dev", "--import-realm"]
