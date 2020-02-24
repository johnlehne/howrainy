# howrainy
Show the estimated chance of rain and estimated amount.  Used to determine rain gear required when biking. 

## Use DigitalOcean's doctl to spin up droplet (VM).

`doctl compute droplet create <name_for_machine> --size s-1vcpu-1gb --region sfo2 --image ubuntu-18-04-x64 --ssh-keys <finger_print_of_pub_key>`

## Run ansible against machine
`ansible-playbook -vvv -i $(doctl compute droplet list --format PublicIPv4 --no-header), playbook.yml -u root --ask-vault-pass`
