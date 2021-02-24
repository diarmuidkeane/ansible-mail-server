# ubuntu-mail-server

### overview
ansible script to build a send only mail server based on this [ recipe provided by digital ocean ] (https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-postfix-as-a-send-only-smtp-server-on-ubuntu-18-04 ) 

### steps

 - create an inverntory file and add your mail server's domain
 
- build the send only mail server with this command ( provide an email for certbot admin contact ) 
        
       ansible-playbook  --user root -e "admin_email=<<certbot admin email address>>" -i inventory mail-send-only.yml


