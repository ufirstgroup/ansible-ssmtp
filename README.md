ansible-ssmtp
=============

Ansible role for installing and configuring sSMTP to deliver local email to a
mail hub. sSMTP is ideal for situations where a full-blown mail transfer agent
such as Postfix, Exim or Sendmail is not desired.

Optimized to be used with Mandrill service (http://mandrill.com/)

Role Variables
--------------

A more detailed description of these options can be found in the
templates/ssmtp_conf.j2 file and templates/revaliases.j2.

  **notification_mail** - Address which is to receive root emails

  **ssmtp_mailhub** - Hostname or IP address of server that will receive emails, do not change default is OK

  **ssmtp_hostname** - Hostname used in SMTP protocol

  **ssmtp_auth_user** - Mandrill username

  **ssmtp_auth_pass** - Mandrill API key

Requirements
-----------

Remember to modify your SPF and DKIM register in the DNS entry of your doamin to use Mandrill as a SMTP relay host.

Dependencies
-----------

Mandrill account.

Installation
----------

ansible-galaxy install oriol.rius.ssmtp-mandrill

    ---
    - hosts: all
      roles:
        - oriol.rius.ssmtp-mandrill

License
------

MIT

Author Information
----------------
Oriol Rius

[GitHub project page](https://github.com/oriolrius/ansible-ssmtp)

based on work of:

Brian Showalter

[GitHub project page](https://github.com/brisho/ansible-ssmtp)
