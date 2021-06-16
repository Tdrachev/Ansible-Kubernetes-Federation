# Ansible-Kubernetes

A repo containing ansible playbooks for deploying and destroying a federation kubernetes cluster

# How to:

1. Create the inventories for your different cluster regions and 1 for your federation controller
2. Run the cluster-creation.yaml playbook with each inventory
3. Run the federation-setup.yaml with --extra-vars "region=NA" or your respective region name
4. Add the path to your certificate-authorities to the $HOME/.kube/config file - usually the locations in which the .crt are saved are /tmp/
5. Run the federation-join.yaml with --extra-vars "region=NA" and you should see the clusters in a federation
