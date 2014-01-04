ansible-ssmtp
=============

Ansible role for installing and configuring sSMTP to deliver local email to a
mail hub. sSMTP is ideal for situations where a full-blown mail transfer agent
such as Postfix, Exim or Sendmail is not desired.

Role Variables
--------------

A more detailed description of these options can be found in the
templates/ssmtp_conf.j2 file.

  ssmtp_root_recipient: admin@example.com   # Address to receive root emails
  ssmtp_mailhub: mailhub.example.com        # Hostname or IP address of mail hub
  ssmtp_rewrite_domain: example.com         # Mail will seem to come from this domain
  ssmtp_from_line_override: NO              # YES/NO - whether to allow user to specify From: address


Requirements
-----------

None

Dependencies
-----------

None

License
------

MIT

Author Information
----------------
Brian Showalter
