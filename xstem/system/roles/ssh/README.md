ssh
=========

Install and configure `ssh`

Requirements
------------

/

Role Variables
--------------

### General variables

| **Name** | **Description** | **Default** |
|----------|-----------------|-------------|
| `ssh_packages` | Mandatory packages for ssh installation | `[ "openssh", "openssh-server" ]` |
| `ssh_packages_extra` | Additional packages for ssh installation | `[]` |
| `ssh_banner_template` | Template file to use for SSH banner | `sshd_banner_default.j2` |
| `sshd_config_template` | Template file to use for SSH daemon config | `sshd_config_default.j2` |
| `ssh_config_template` | Template file to use for SSH client config | `ssh_config_default.j2` |

### SSH client config

| **Name** | **Description** | **Default** |
|----------|-----------------|-------------|
| `ssh_includes` | SSH config `Include` | `[ "/etc/ssh/ssh_config.d/*.conf" ]` |
| `ssh_config_extra` | Extra config lines | `[ "# No extra config" ]` |

### SSH daemon config

| **Name** | **Description** | **Default** |
|----------|-----------------|-------------|
| `sshd_includes` | SSH config `Include` | `[ "/etc/ssh/sshd_config.d/*.conf" ]` |
| `sshd_port` | SSH config `Port` | `"22"` |
| `sshd_address_family` | SSH config `AddressFamily` | *None* |
| `sshd_listen_address` | SSH config `ListenAddress` | *None* |
| `sshd_permit_open` | SSH config `PermitOpen` | *None* |
| `sshd_protocol` | SSH config `Protocol` | *None* |
| `sshd_host_keys` | SSH config `HostKey` | `[]` |
| `sshd_rekey_limit` | SSH config `RekeyLimit` | *None* |
| `sshd_key_regeneration_interval` | SSH config `KeyRegenerationInterval` | *None* |
| `sshd_syslog_facility` | SSH config `SyslogFacility` | *None* |
| `sshd_loglevel` | SSH config `LogLevel` | *None* |
| `sshd_login_grace_time` | SSH config `LoginGraceTime` | *None* |
| `sshd_permit_root_login` | SSH config `PermitRootLogin` | *None* |
| `sshd_strict_mode` | SSH config `StrictModes` | *None* |
| `sshd_max_auth_tries` | SSH config `MaxAuthTries` | *None* |
| `sshd_max_sessions` | SSH config `MaxSessions` | *None* |
| `sshd_rsa_authentication` | SSH config `RSAAuthentication` | *None* |
| `sshd_pubkey_authentication` | SSH config `PubkeyAuthentication` | *None* |
| `sshd_authorize_keys_file` | SSH config `AuthorizedKeysFile` | `".ssh/authorized_keys"` |
| `sshd_ciphers` | SSH config `Ciphers` | *None* |
| `sshd_authorized_principals_file` | SSH config `AuthorizedPrincipalsFile` | *None* |
| `sshd_authorized_keys_command` | SSH config `AuthorizedKeysCommand` | *None* |
| `sshd_authorized_keys_command_user` | SSH config `AuthorizedKeysCommandUser` | *None* |
| `sshd_host_based_authentication` | SSH config `HostbasedAuthentication` | *None* |
| `sshd_host_based_uses_name_from_packet_only`%} | SSH config `HostbasedUsesNameFromPacketOnly` | *None* |
| `sshd_ignore_user_know_hosts` | SSH config `IgnoreUserKnownHosts` | *None* |
| `sshd_ignore_rhosts` | SSH config `IgnoreRhosts` | *None* |
| `sshd_password_authentication` | SSH config `PasswordAuthentication` | `"no"` |
| `sshd_permit_empty_passwords` | SSH config `PermitEmptyPasswords` | *None* |
| `sshd_kbd_interactive_authentication` | SSH config `KbdInteractiveAuthentication` | *None* |
| `sshd_kerberos_authentication` | SSH config `KerberosAuthentication` | *None* |
| `sshd_kerberos_or_local_passwd` | SSH config `KerberosOrLocalPasswd` | *None* |
| `sshd_kerberos_ticket_cleanup` | SSH config `KerberosTicketCleanup` | *None* |
| `sshd_kerberos_get_afs_token` | SSH config `KerberosGetAFSToken` | *None* |
| `sshd_kerberos_use_kuserok` | SSH config `KerberosUseKuserok` | *None* |
| `sshd_gssapi_authentication` | SSH config `GSSAPIAuthentication` | *None* |
| `sshd_gssapi_cleanup_credentials` | SSH config `GSSAPICleanupCredentials` | *None* |
| `sshd_gssapi_strict_acceptor_check` | SSH config `GSSAPIStrictAcceptorCheck` | *None* |
| `sshd_gssapi_key_exchange` | SSH config `GSSAPIKeyExchange` | *None* |
| `sshd_gssapi_enable_k5_users` | SSH config `GSSAPIEnablek5users` | *None* |
| `sshd_use_pam` | SSH config `UsePAM` | `"no"` |
| `sshd_deny_users` | SSH config `DenyUsers` | *None* |
| `sshd_allow_users` | SSH config `AllowUsers` | *None* |
| `sshd_deny_groups` | SSH config `DenyGroups` | *None* |
| `sshd_allow_groups` | SSH config `AllowGroups` | *None* |
| `sshd_allow_agent_forwarding` | SSH config `AllowAgentForwarding` | *None* |
| `sshd_allow_tcp_forwarding` | SSH config `AllowTcpForwarding` | *None* |
| `sshd_gateway_ports` | SSH config `GatewayPorts` | *None* |
| `sshd_x11_forwarding` | SSH config `X11Forwarding` | *None* |
| `sshd_x11_display_offset` | SSH config `X11DisplayOffset` | *None* |
| `sshd_x11_use_localhost` | SSH config `X11UseLocalhost` | *None* |
| `sshd_permit_tty` | SSH config `PermitTTY` | *None* |
| `sshd_print_motd` | SSH config `PrintMotd` | `"yes"` |
| `sshd_print_last_log` | SSH config `PrintLastLog` | *None* |
| `sshd_tcp_keep_alive` | SSH config `TCPKeepAlive` | *None* |
| `sshd_permit_user_environment` | SSH config `PermitUserEnvironment` | *None* |
| `sshd_compression` | SSH config `Compression` | *None* |
| `sshd_client_alive_interval` | SSH config `ClientAliveInterval` | *None* |
| `sshd_client_alive_count_max` | SSH config `ClientAliveCountMax` | *None* |
| `sshd_use_dns` | SSH config `UseDNS` | *None* |
| `sshd_pid_file` | SSH config `PidFile` | *None* |
| `sshd_max_startups` | SSH config `MaxStartups` | *None* |
| `sshd_permit_tunnel` | SSH config `PermitTunnel` | *None* |
| `sshd_challenge_response_authentication` | SSH config `ChallengeResponseAuthentication` | *None* |
| `sshd_chroot_directory` | SSH config `ChrootDirectory` | *None* |
| `sshd_version_addendum` | SSH config `VersionAddendum` | *None* |
| `sshd_force_command` | SSH config `ForceCommand` | *None* |
| `sshd_banner` | SSH config `Banner` | `"/etc/ssh/sshd_banner"` |
| `sshd_accept_env` | SSH config `AcceptEnv` | `"LANG LC_*"` |
| `sshd_subsystem` | SSH config `Subsystem` | `"sftp /usr/libexec/openssh/sftp-server"` |
| `sshd_config_extra` | Extra config lines | `[ "# No extra config" ]` |

Dependencies
------------

/

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
    - { role: ssh }

```

License
-------

MIT

Author Information
------------------

Gautier Miquet <xisabla.dev@gmail.com>
