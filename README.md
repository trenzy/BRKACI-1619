# BRKACI-1619
Ansible Playbooks associated with Cisco Live session BRKACI-1619 (Automating ACI with Ansible)

These playbooks are the playbooks that are demoed during the Cisco Live session BRKACI-1619. Most of these have been tested 
on the following ACI versions:

3.2(4d)
3.2(5d)
4.2(2f)

The following Ansible versions were used with these:

2.8
2.9

They cover the following:

bp.yml - This is an example of using the aci_rest module to configure some Cisco ACI Best Practices

ciscolive.yml - An example of configuring an ACI Tenant called CiscoLive. This uses the standard username/password. 

external_vars.yml - External variables that are used with the three tier application playbook.

push-cert.yml - Playbook to push signature-based certificates to the APIC so that they will be used in playbooks in place of username/passwords.

tenant.yml - Playbook to create a Tenant called Cert. This playbook uses signature-based authentication.
three-tier.yml - Playbook to build a full three tier application leveraging the external_vars.yml file. It creates the tenant, vrf, and Bridge Domain. It then creates 3 EPGs (web, app, DB) and also creates the contract associations for them in including subjects and filters.
