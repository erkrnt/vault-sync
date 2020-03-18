# vaultsync

## Example

Below is a basic example of how to use `vaultsync`.

### Config

The configuration file is the main source for `vaultsync` and is used to set the source and target Vault servers including their engines w/ secrets.

```
{
  "vault_secrets": [
    {
      "engine": "kv",
      "mount": "example/",
      "options": {
        "version": "1"
      },
      "paths": ["localhost/api", "localhost/cron", "localhost/discord"]
    }
  ],
  "vault_source_addr": "http://localhost:8300",
  "vault_source_token": "<vault-source-token>",
  "vault_target_addr": "http://localhost:8200",
  "vault_target_token": "<vault-target-token>"
}
```

### Run

To run the program, put a `config.json` in the same directory as the source code or use the CLI arg `--config=` to set your file at run-time.

```
vaultsync --config="./config.json"
```
