# Grafana opensearch plugin test environment

Made for this issue https://github.com/grafana/opensearch-datasource/issues/487

## Usage

1. Run `docker compose up` to launch everything.
2. Wait until the stream of log messages ends.
3. Go to http://localhost:3000 (grafana) and login with keycloak
4. Enter username "admin" and password "admin".
5. Install opensearch plugin.
6. Add opensearch datasource. Make sure to toggle "Forward OAuth Identity" on. Use `http://opensearch-proxy:9200` as the address.
7. Try making a query via explore and observe logs from the proxy.
8. To confirm that everything is working add "elasticsearch" datasource with the same settings (host and forward identity). You should be able to perform queries with it.
