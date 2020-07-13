Role Name
=========

This role creates a load-sharing mirror for the SVM_root

Requirements
------------

This role is dependant upon an SVM having been previously created. 

Role Variables
--------------

---
# defaults file for ls_mirror
ls_mirrors:
    - { ls_source_volume: "svm_root",  # 
        size: 1, 
        size_unit: gb, 
        source_svm: "svmData", 
        ls_destination_volume: "svmData_root_LS", 
        destination_svm: "svmData", 
        destination_aggregate: "aggr_data1", 
        schedule: "5min", 
        lsupdate: "N" }

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
