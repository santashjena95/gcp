# gcp/vault
Terraform and Ansible script to deploy Vault 0.10.1 (Vanilla-configured, single instance, Initialized) within a GCP instance.

Requirements: Terraform and Ansible locally installed. GCP project, Service Account JSON file and Project wide SSH Key.

Ounce deployed, Vault will be Initialized. You can check the status with the following steps:

* SSH to your instance
* export VAULT_ADDR=http://127.0.0.1:8200 (Change IP to be your private IP)
* vault status
* Define a firewall rule to allow ingress on 8200
* http://public_IP:8200/ui
