Role Name
=========

A brief description of the role goes here.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

 The following variables are required
 - activation_key
 - org_id
 - install_EPEL

 I recomend includding this is the play that calls this role:

 ----------------------------8<--------------------------------


 ---------------------------->8----------------------------------

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

- name: Host preparation
  hosts: hosts
  vars:
    pool_name: "Employee SKU"
  vars_prompt:
    - name: "activation_key"
      prompt: "Type your activation key"
      private: no
    - name: "org_id"
      prompt: "Type your org id"
      private: no
    - name: "install_EPEL"
      prompt: "Would you like to install EPEL packages ? True/False"
      private: no
  roles:
    - rhel

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
