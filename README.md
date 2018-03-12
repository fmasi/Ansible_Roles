The following variables are required
- activation_key
- org_id
- install_EPEL

I recomend includding this is the play that calls this role:

----------------------------8<--------------------------------
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
    
---------------------------->8----------------------------------
