# Ansible Role



## Purpose
  Prepare server for Rancher Kubernetes Engine (rke).
  
----

## Execution
<pre>
    - hosts: all
      tasks:
      - include_role:
          name: drewgwallace.ansible-role-prep_rke
        vars:
          path_to_ssh_pub_key: "/home/<b>USER</b>/.ssh/id_rsa.pub"
          docker_version: "17.03.2~ce~3-0~ubuntu"
</pre>

----

## Notes
+ Debian based servers with Apt type package management ONLY
+ [RKE supported](https://rancher.com/docs/rke/v0.1.x/en/installation/os/) versions aren't found in the docker repository for Ubuntu bionic at this time, the install will fail unless using something unsupported such as "18.03.1~ce~3-0~ubuntu"
