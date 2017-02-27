## Introduction

This Ansible role will setup an IPSec/L2TP vpn server with Ubuntu 14.04 using Openswan as IPSec server, use xl2tpd as the l2tp provider and ppp as user authentication. 


## Tested Environment
- Ubuntu 14.04.5 LTS (Trusty Tahr)


## Usage
- Setup VPS instance and with private ip, associate elastic ip or public IP
- Modify the variables in 'default/main.yml'
- Alternatively, you can input variable via ansible-playbook "--extra-vars" parameters 
- Then you need manually adding users and passwd to /etc/ppp/chap-secrets


## Variables
- instance\_private\_ip: Instance private IP in your VPC
- shared\_secret\_value: The shared secret in machine authentication
- lns\_ip\_range: IP range for VPN client in separate vpn network
- lns\_local\_ip: IP for the VPN server in separate VPN network
- ms-dns\_first: public or private DNS server which you can used google public dns as default


## References
- [https://raymii.org/s/tutorials/IPSEC_L2TP_vpn_with_Ubuntu_14.04.html](https://raymii.org/s/tutorials/IPSEC_L2TP_vpn_with_Ubuntu_14.04.html)
- [https://www.youtube.com/watch?v=DoYVkapRUno](https://www.youtube.com/watch?v=DoYVkapRUno)
- [http://www.iptables.info/en/iptables-targets-and-jumps.html#MASQUERADETARGET](http://www.iptables.info/en/iptables-targets-and-jumps.html#MASQUERADETARGET)

