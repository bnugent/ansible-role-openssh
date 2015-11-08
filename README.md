Role Name
=========

This role installs and configures OpenSSH client and server on Ubuntu. The
default configuration is based on the [Secure Secure
Shell](https://stribika.github.io/2015/01/04/secure-secure-shell.html) blog
post by [stribika](https://github.com/stribika).


Role Variables
--------------

* `openssh_client_pkg_name` - Name of the OpenSSH client package
* `openssh_client_pkg_state` - OpenSSH client package state
* `openssh_client_config_enable_github` - GitHub sometimes needs different ciphers
* `openssh_client_config_kexalgorithms` - Key exchange algorithms this client supports
* `openssh_client_config_passwordauthentication` - Whether to enable password authentication
* `openssh_client_config_pubkeyauthentication` - Whether to enable public key authentication
* `openssh_client_config_hostkeyalgorithms` - Host key algorithms for connections from this host
* `openssh_client_config_ciphers` - Supported ciphers for client connections from this host
* `openssh_client_config_macs` - Message authentication codes for client connections from this host
* `openssh_server_pkg_name` - Name of the OpenSSH server package
* `openssh_server_pkg_state` - OpenSSH server package state
* `openssh_server_config_usergroup` - Group name of user group permitted to access this host
* `openssh_server_config_kexalgorithms` - Key exchange algorithms this server supports
* `openssh_server_config_passwordauthentication` - Enable or disable password authentication to this server
* `openssh_server_config_pubkeyauthentication` - Enable or disable public key authentication to this server
* `openssh_server_config_ciphers` - Supported ciphers
* `openssh_server_config_macs` - Supported message authentication codes
* `openssh_server_config_port` - Server listen port
* `openssh_server_config_listenaddress` - Server listen addresses
* `openssh_server_config_loglevel` - Server log level
* `openssh_server_config_permitrootlogin` - Enable or disable logins from the root user
* `openssh_server_config_strictmodes` - Enable or disable strict file mode checking
* `openssh_server_config_challengeresponseauthentication` - Enable or disable challenge response authentication
* `openssh_server_config_usepam` - Enable or disable PAM
* `openssh_server_config_x11forwarding` - Enable or disable X11 forwarding
* `openssh_server_config_maxauthtries` - Maximum number of authentication attempts per connection
* `openssh_server_config_clientaliveinterval` - Interval in seconds after which a message is sent to the client to see if its alive
* `openssh_server_config_clientalivecountmax` - Number of client alive messages that will be sent
* `openssh_server_regenerate_host_keys` - Whether to regenerate the distro-provided default host keys
* `openssh_server_service_name` - Name of the OpenSSH server daemon
* `openssh_server_service_enabled` - Enable or disable OpenSSH server on boot
* `openssh_server_service_state` - OpenSSH server daemon state

Dependencies
------------

none

Example Playbook
----------------

    - hosts: servers
      roles:
         - openssh

License
-------

MIT

Author Information
------------------

Role created by Ben Nugent.
