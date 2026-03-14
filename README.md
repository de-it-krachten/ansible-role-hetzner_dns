[![CI](https://github.com/de-it-krachten/ansible-role-hetzner_dns/workflows/CI/badge.svg?event=push)](https://github.com/de-it-krachten/ansible-role-hetzner_dns/actions?query=workflow%3ACI)


# ansible-role-hetzner_dns

Setup DNS domain in Hetzner
<basic role description>



## Dependencies

#### Roles
None

#### Collections
- community.dns

## Platforms

Supported platforms

- Red Hat Enterprise Linux 8<sup>1</sup>
- Red Hat Enterprise Linux 9<sup>1</sup>
- Red Hat Enterprise Linux 10<sup>1</sup>
- RockyLinux 8
- RockyLinux 9
- RockyLinux 10
- OracleLinux 8
- OracleLinux 9
- OracleLinux 10
- AlmaLinux 8
- AlmaLinux 9
- AlmaLinux 10
- Debian 11 (Bullseye)
- Debian 12 (Bookworm)
- Debian 13 (Trixie)
- Ubuntu 22.04 LTS
- Ubuntu 24.04 LTS
- Fedora 42
- Fedora 43

Note:
<sup>1</sup> : no automated testing is performed on these platforms


## Role Variables
### defaults/main.yml
<pre><code>
# Hetzner API token
# hetzner_dnsapi_token: your-token

# Hetzner zone name
# hetzner_zone_name: your-zone

# Hetzner zone API
hetzner_zone_url: "https://dns.hetzner.com/api/v1/zones"

# DNS records
hetzner_dns_records: []

# Hetzner DNS servers
hetzner_nameservers:
  - hydrogen.ns.hetzner.com
  - oxygen.ns.hetzner.com
  - helium.ns.hetzner.de
</pre></code>




## Example Playbook
### molecule/default/converge.yml
<pre><code>
- name: sample playbook for role 'hetzner_dns'
  hosts: all
  become: 'yes'
  tasks:
    - name: Include role 'hetzner_dns'
      ansible.builtin.include_role:
        name: hetzner_dns
</pre></code>
