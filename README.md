# freeipa_ansible
there are 2 playbooks inside roles directory.
1- ipa_server 2- ipa_client
steps to run configure feeeIPA server
i) first we need to configure hostname for server and client
in my case hostname of sevrer: ipa.meesho.com and client: ipa-client
ii) configure route 53 entry for ipa.meesho.com
iii) make changes in the file roles/ipa_server/defaults/main.yml

iv) run below command to configure IPAserver
ansible-playbook ipa-server.yml

v) after successfull installation, open the url in browser

ipa.meesho.com (please mentioned your dns entry)

steps to run configure feeeIPA client

i) check if client machine hostname configure correctly
ii) make changes in the file roles/ipa_client/defaults/main.yml
iii) run below command
ansible-playbook ipa-client.yml
iv) open ipa.meesho.com and check if client has been reflecting in host section.
v) now try to login from your local to ipa-client machine using admin credentials which we configured in roles/ipa_server/defaults/main.yml

