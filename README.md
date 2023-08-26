# Datadog

This section there is a intention to help someone in setting up a Datadog Cluster Agent in Kubernets Cluster. So I used the Ansible language to automate these processes.

Step 1:
>Configure host bastion that you are using.
>
Step 2:
>Setting your API Key and App Key (This stuff can find in: Organization Settings -> Access -> API KEY/APP KEY) in VARS/main.yaml
```
dd_api_key_name: DD_API_KEY
dd_api_key_value: <api_key>
dd_app_key_name: DD_APP_KEY
dd_app_key_value: <app_key>
```
>
Step 3:
>Configure Cluster API, Username and Password of your cluster Kubernets:
```
- name: Create Secret Datadog API KEY
  openshift_login:
  username: <username>
  password: <password>
  server_url: <openshift_api>
  validate_certs: no
```
