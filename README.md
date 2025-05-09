# Data Disclosure
IMC 2025 paper submission data disclosure

This archive (`Archive.zip`, **504MB**) unpacks to approximately **8.1GB** of log files.

| Interaction | DBMS       | Port  | #   | Customization                                 | Log                         | Honeypot                                                              |
|:------------|:------------|:-------|:-----|:----------------------------------------------|:----------------------------|:----------------------------------------------------------------------|
| Low        | MySQL      | 3306  | 50  | Default (One of eachhoneypot instance per VM) | qeeqbox_default.json        | [Qeeqbox](https://github.com/qeeqbox/honeypots)                       |
| Low        | PostgreSQL | 5432  | 50  | Default                                       | qeeqbox_default.json        | [Qeeqbox](https://github.com/qeeqbox/honeypots)                       |
| Low        | Redis      | 6379  | 50  | Default                                       | qeeqbox_default.json        | [Qeeqbox](https://github.com/qeeqbox/honeypots)                       |
| Low        | MSSQL      | 1433  | 50  | Default                                       | qeeqbox_default.json        | [Qeeqbox](https://github.com/qeeqbox/honeypots)                       |
| Low        | MySQL      | 3306  | 5   | Single honeypot instance per VM               | qeeqbox_single.json         | [Qeeqbox](https://github.com/qeeqbox/honeypots)                       |
| Low        | PostgreSQL | 5432  | 5   | Single honeypot per instance                  | qeeqbox_single.json         | [Qeeqbox](https://github.com/qeeqbox/honeypots)                       |
| Low        | Redis      | 6379  | 5   | Single honeypot per instance                  | qeeqbox_single.json         | [Qeeqbox](https://github.com/qeeqbox/honeypots)                       |
| Low        | MSSQL      | 1433  | 5   | Single honeypot per instance                  | qeeqbox_single.json         | [Qeeqbox](https://github.com/qeeqbox/honeypots)                       |
| Medium     | Redis      | 6379  | 10  | Default                                       | redis_default.log           | [RedisHoneyPot](https://github.com/cypwnpwnsocute/RedisHoneyPot)      |
| Medium     | Redis      | 6379  | 10  | Fake data                                     | redis_fake_data.log         | [RedisHoneyPot](https://github.com/cypwnpwnsocute/RedisHoneyPot)      |
| Medium     | PostgreSQL | 5432  | 10  | Default                                       | postgres_default.log        | [Sticky Elephant](https://github.com/betheroot/sticky_elephant)       |
| Medium     | PostgreSQL | 5432  | 10  | Login disabled                                | postgres_login_disabled.log | [Sticky Elephant](https://github.com/betheroot/sticky_elephant)       |
| Medium     | Elastic    | 9200  | 10  | Default                                       | elasticpot.json             | [ElasticPot](https://gitlab.com/christian.wahl/elasticpot)            |
| High       | MongoDB    | 27017 | 8   | Fake data                                     | mongodb-XX.log              | [monodb-honeypot](https://github.com/AquilaIrreale/mongodb-honeypot)  |

Refer to table above for a detailed mapping of the log files, configurations, and their respective honeypots.

## Anonymization

All IP addresses in the format `192.168.0.x` were internal to our network and have been anonymized to protect our infrastructure.

## Log Files Overview

The archive contains _RAW_ logs from multiple honeypots and configurations, organized as follows:

### Qeeqbox Honeypot Logs
These are the logs for the low-interaction honeypots:

- `qeeqbox_default.json` — Logs from the default Qeeqbox configuration.  
- `qeeqbox_single.json` — Logs from the "single" configuration.

### Redis Honeypot Logs

- `redis_default.log` — Logs from the default Redis configuration.  
- `redis_fake_data.log` — Logs from the configuration with fake data.

### PostgreSQL Honeypot Logs

- `postgres_default.log` — Logs from the default PostgreSQL configuration.  
- `postgres_login_disabled.log` — Logs from the configuration with login disabled.

### Elasticpot Logs

- `elasticpot.json` — Contains log entries from the Elasticpot honeypot.

### MongoDB Honeypot Logs

Log files are organized by country code:

- `mongodb-AU.log` — Australia  
- `mongodb-CA.log` — Canada  
- `mongodb-DE.log` — Germany  
- `mongodb-IN.log` — India  
- `mongodb-NL.log` — Netherlands  
- `mongodb-SG.log` — Singapore  
- `mongodb-UK.log` — United Kingdom  
- `mongodb-US.log` — United States  
