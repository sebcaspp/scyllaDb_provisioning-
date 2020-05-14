

ansible-playbook --ask-become-pass --verbose --ask-pass  node-playbook.yml


#to create a token
kubeadm token create --print-join-command
- the result should be somethin like  -> kubeadm join 192.168.1.101:6443 --token ie0p33.vkq8mhhkjbvwnyvf     --discovery-token-ca-cert-hash sha256:4880a7aa7313453824723af0a7e00f770cd554dfaacfa3e6d67ab63b08be43a0 

# to list a tokens
kubeadm token list