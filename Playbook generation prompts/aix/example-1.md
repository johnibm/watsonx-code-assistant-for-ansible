#### **How to access Playbook Generation?**
Click on the **'Ansible'** icon on VS Code's Activity Bar  
Under **'Ansible Content Creator'** -> **'Get Started'**  
Under **'Create'** -> **'Playbook with Ansible Lightspeed'**

**🎯 Copy the content below and paste into the textarea.**

```yaml
Create a playbook to apply update patches to AIX servers with the following steps:
1. Print on screen using 'start_msg' var
2. Performs an in-depth consistency check on the installed LPPs(lppchk -vm3)
3. Assert the length of the stdout output in the previous task is equal to zero with a custom message 'assert_lppchk_msg' var
4. Ensure directory exist {{ mount_over_dir_value }}
5. Mount NFS share using ibm.power_aix.mount module with vars 'node_v', 'mount_dir_value' and 'mount_over_dir_value'
6. Check the currently OS version(oslevel -s)
7. List interim fix using ibm.power_aix.emgr module and register the output
8. Remove all interim fix using ibm.power_aix.emgr module based on 'ifix_label' if it found any in the previous task
9. Commit all filesets with applied state using ibm.power_aix.installp module with the commit action and install_list all
10. Updating to a new Technology Level or Service Pack using install_all_updates with device as 'target_dir', 'extend_fs', 'agree_licenses' and 'suppress_multivolume' var
11. Assert string 'install_all_updates: Result = SUCCESS' in output(STDOUT) at previous task with a custom message 'dict_update_tl_sp_msg' var
12. Reboot host(s) using ibm.power_aix.reboot module when install_all_updates_result
13. Notify Slack with token as 'vars_token', msg as 'vars_msg and color as 'vars_color' when vars_slack_token is defined
14. Umount NFS share using the ibm.power_aix.mount module with the variable 'mount_dir_value' and 'force'
15. Print on screen using 'final_msg' var
```

- Press **"Analyze"** to proceed.
- **Review the suggested steps for your playbook and modify as needed.** _(Prompt refinement)_
- Press **"Generate playbook"** to open a new tab file with the full playbook.

**Note:** _The feature exclusively creates **self-contained** Full Playbooks — it does not generate Ansible roles._