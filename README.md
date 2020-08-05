**DISCLAIMER**:
   I've tested this playbook in my Satellite network using a vanilla RHEL **7.8**. 
   **DO NOT USE THIS IN PRODUCTION HOST**
   
**PREREQUISITE**:
You need to make sure that the following are promoted in the Content View (CV) of the Host

Red Hat Enterprise Linux 8 for x86_64 - BaseOS RPMs **8.2** 

Red Hat Enterprise Linux 8 for x86_64 - AppStream RPMs **8.2**

Red Hat Enterprise Linux 8 for x86_64 - Supplementary RPMs **8.2**

**Instructions**
By default, the playbook will run against **localhost**

1. yum -y install ansible git
2. git clone this repo
3. Edit the inventory file if you need to run the playbook to a different host. 
4. ansible-playbook -i inventory upgrade_rhel7.yaml
5. #4 will attempt to update the host and reboot. 
6. If it skips the reboot portion, you just have to wait until the **leapp upgrade** tasks is finished then reboot. Else, run #4 again to continue.


