# $`\textcolor{red}{\text{ElasticsearchRole}}`$ #

Ansible Role: elasticsearch
An ansible role to install and configure elasticsearch  setup.

# $`\textcolor{voilet}{\text{Supported OS}}`$ #
* Redhat : 9
* Ubuntu : 16/18/20
# $`\textcolor{voilet}{\text{Dependencies}}`$ #
* python

# $`\textcolor{voilet}{\text{Role Variables/Defaults}}`$ #

| Variables            | Default values| Description|
| -------------        | ------------- | -------- |
| major_version        | "7"             |version series number which you want to install|
| minor_version        | "7.17.0"        | Elasticsearch version you want to install  |
| debian_GPP_key       | https://artifacts.elastic.co/GPG-KEY-elasticsearch|  GPG key link|
| redhat_GPG_key       | https://artifacts.elastic.co/GPG-KEY-elasticsearch| PGP key link|
| path_for_data        | /var/lib/elasticsearch | path for elasticsearch data |
| path_for_logs        | /var/log/elasticsearch | path for elasticsearch logs |
| http_port            | 9200                   | Default port for elasticsearch |


# $`\textcolor{voilet}{\text{Sample Inventory}}`$ 
An inventory for elasticsearch setup should look like this:-
```shell
* node1 ansible_host=3.18.109.204 ansible_user=ubuntu ansible_ssh_private_key_file=/home/sunil/Downloads/Elastic.pem
* node2 ansible_host=3.16.147.112 ansible_user=ubuntu ansible_ssh_private_key_file=/home/sunil/Downloads/Elastic.pem
```
# $`\textcolor{voilet}{\text{Sample Playbook}}`$
### $`\textcolor{voilet}{\text{Here is an example playbook:-}}`$ 
```shell
---
- hosts: all
  become: yes
  roles:
    - es_role
```
### $`\textcolor{red}{\text{ansible-playbook -i inventory master.yml }}`$

## $`\textcolor{voilet}{\text{Elasticsearch running on Debian system}}`$
![image.png](./image.png)



# $`\textcolor{red}{\text{Author Information}}`$ 
# $`\textcolor{green}{\text{Sunil kumar}}`$

