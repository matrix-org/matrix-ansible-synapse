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
| **matrix_synapse_tls_cert** | __string__ | server's TLS certificate chain (_when matrix_synapse_extra_config.no_tls is set to true_)|
| **matrix_synapse_tls_key** | __string__ | server's TLS key (_when matrix_synapse_extra_config.no_tls is set to true_)|
| **matrix_synapse_report_stats** | __bool__ | Report the stats to matrix.org |
| **matrix_synapse_pg_host** | __sting__ | postgresql server |
| **matrix_synapse_pg_user** | __string__ | postgresql user |
| **matrix_synapse_pg_pass** | __string__ | postgresql user's password |
| **matrix_synapse_pg_db** | __string__ | postgresql database |

### Optional Variables

| Name | Value | Description |
| :--- | :--- | :---  |
| matrix_synapse_base_path | "/opt/synapse" | 
| matrix_synapse_secrets_path | "{{ matrix_synapse_base_path }}/secrets"
| matrix_synapse_extra_config | _None_ | configuration parameters as given in the [synapse configuration file](https://github.com/matrix-org/synapse/tree/master/docs) | 
| matrix_synapse_dh_path | "{{ matrix_synapse_base_path }}/tls/{{ matrix_server_name }}.dh" |
| matrix_synapse_baseurl | "https://{{ matrix_server_name }}" |
| matrix_synapse_signing_key_path | "{{ matrix_synapse_base_path }}/ssl/{{ matrix_server_name }}.signing.key" |
| matrix_synapse_version | "v0.99.3" |
| matrix_synapse_log_days_keep | 30 |
| matrix_synapse_deployment_method | pip | Either pip or docker [¹](#footnote_1) |
| matrix_synapse_supervision_method | systemd | Either systemd, runit or docker [¹](#footnote_1) |
| matrix_synapse_python_version | 3 | Default python version (2, 3) to be used |

<a name="footnote_1">¹</a>: Docker must be used for both or neither deployment and supervision

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
