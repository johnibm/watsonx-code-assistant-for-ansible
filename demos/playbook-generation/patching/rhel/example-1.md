#### **How to access Playbook Generation?**  
Click on the **'Ansible'** icon on VS Code's Activity Bar  
Under **'Ansible Content Creator'** -> **'Get Started'**  
Under **'Create'** -> **'Playbook with Ansible Lightspeed'**

**🎯 Copy the content below and paste into the textarea.**

```yaml
Create an Ansible playbook to patch RHEL Linux servers in one workflow, disable facts and them perform the following tasks:
Print a debug message saying 'Patching RHEL is starting.'
Get subscription identity(subscription-manager identity)
Fail if the system is not registered.
Get the available repositories for RPM package connectivity and check for any issues.
Fail the playbook if any repositories have problems.
Get space for the disk-based boot file system (/boot)
Fail if the disk-based boot file system (/boot) doest not have at least 100Mb of free space.
Unset the release version used by RHSM repositories, allowing updates to the latest version.
Update all installed packages to the latest versions.
Ensure the RPM package 'yum-utils' is installed.
Check if a reboot is required
Reboot the system to fully integrate all patches into the system if necessary.
Finally, print a message that says 'Patching RHEL has been successfully completed.'
```

- Press **"Analyze"** to proceed.
- **Review the suggested steps for your playbook and modify as needed.** _(Prompt refinement)_
- Press **"Generate playbook"** to open a new tab file with the full playbook.

**Note:** _The feature exclusively creates **self-contained** Full Playbooks — it does not generate Ansible roles._
