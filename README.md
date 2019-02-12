# matrix-synapse

Install a matrix synapse server.

## Requirements

The following should be present on the target system
* `pip`
* `systemd`
* `rsyslogd`
* `logrotate`

## Role Variables

### Mandatory Variables

| Name | Type | Description |
| :--- | :--- | :--- |
| **matrix_server_name** | __string__ | |
| **matrix_synapse_tls_cert** | __string__ | server's TLS certificate chain |
| **matrix_synapse_tls_key** | __string__ | server's TLS key |
| **matrix_synapse_report_stats** | __bool__ | Report the stats to matrix.org |

### Optional Variables

| Name | Value |
| :--- | :---  |
| matrix_synapse_tls_cert_path | "/opt/synapse/tls/{{ matrix_server_name }}.crt" |
| matrix_synapse_tls_key_path | "/opt/synapse/tls/{{ matrix_server_name }}.key" |
| matrix_synapse_dh_path | "/opt/synapse/tls/{{ matrix_server_name }}.dh" |
| matrix_synapse_server_name | "{{ matrix_server_name }}" |
| matrix_synapse_baseurl | "https://{{ matrix_server_name }}" |
| matrix_synapse_pg_pass | "{{ matrix_pg_pass }}" | 
| matrix_synapse_pg_user | "{{ matrix_pg_user }}" |
| matrix_synapse_pg_db | "{{ matrix_pg_db }}" |
| matrix_synapse_pg_host | "{{ matrix_pg_host }}" |
| matrix_synapse_log_config | "/opt/synapse/{{ matrix_server_name }}.log.config" |
| matrix_synapse_media_store_path | "/opt/synapse/media_store" |
| matrix_synapse_uploads_path | "/opt/synapse/uploads" |
| matrix_synapse_turn_secret | "{{ matrix_turn_secret }}" |
| matrix_synapse_turn_uri | "{{ matrix_turn_uri }}" |
| matrix_synapse_registration_secret | "{{ matrix_registration_secret }}" |
| matrix_synapse_macaroon_secret_key | "{{ matrix_macaroon_key }}" |
| matrix_synapse_signing_key_path | "/opt/synapse/ssl/{{ matrix_server_name }}.signing.key" |
| matrix_synapse_version | "v0.34.1.1" |
| matrix_synapse_log_days_keep | 30 |
| matrix_synapse_skip_ssl | false |
| matrix_synapse_pid_file | /opt/synapse/synapse.pid |
| matrix_synapse_manhole | false |
| matrix_synapse_max_upload_size | 23M |
| matrix_synapse_url_preview_enabled | true |
| matrix_sybapse_registration_secret | __randomly generated__ |

## Dependencies

__None__.

## Example Playbook

```yaml
#TODO: Add example
```

## License

Apache 2.0

# Author Information

* Michael Kaye
* Jan Christian Grünhage
* Emmanouil Kampitakis
