# Ansible Role: FreshRSS

Installs FreshRSS and sets up database backups

## Requirements

This role assumes the following:

* Docker is installed

## Role Variables

### Main Variables

| Name | Default Value | Details |
| --- | --- | --- |
| `freshrss_version` |  | The version of the FreshRSS Dockerfile to use. More versions available [here]() |
| `freshrss_database_password` |  | The user password for the DB |
| `freshrss_listen_host` | `0.0.0.0` | The interface FreshRSS listens on |
| `freshrss_listen_port` | 8081 | The port FreshRSS listens on |
| `freshrss_cron_minutes` | `13,43` | When to run the FreshRSS feed checks (every hour at these minutes) |
| `freshrss_database_username` | `freshrss` | Database username |
| `freshrss_database_version` | `12.5` | Version of the PostgreSQL container to use |


### Default Variables

(Don't change these unless you really have to!)

| Name | Default Value | Details |
| --- | --- | --- |
| `app_name` | `freshrss` | Used to name things |
| `app_folder` | `/apps/freshrss` | The base directory for deployment |
| `freshrss_listen` | Based on `freshrss_listen_*` above | The listen address for FreshRSS |

## Dependencies

None

## License

MIT
