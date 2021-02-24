# ubuntu-mail-server

### ansible script to build a send only mail server based on this recipe provided by digital ocean 

### steps

 - create an inverntory file and add your mail server's domain
 
- build the send only mail server with this command ( provide an email for certbot admin contact ) 
        
       ansible-playbook  --user root -e "admin_email=<<certbot admin email address>>" -i inventory mail-send-only.yml


