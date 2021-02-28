# ubuntu-mail-server

### overview
ansible script to build mail server in various configurations 

 - send only mail server based on this [recipe provided by digital ocean](https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-postfix-as-a-send-only-smtp-server-on-ubuntu-18-04) 
 - forward only mail server -  variation on the above to allow incoming mail to be forwarded to another email recipient

### steps

 - create an inverntory file and add your mail server's domain
 
- build the send only mail server with this command ( provide an email addresses for certbot admin contact and root alias ) 
        
       ansible-playbook  --user root -e "admin_email=<<certbot admin email address>> root_email_alias=<<email alias for root user>>" -i inventory mail-send-only.yml

- build the forward only mail server with this command ( provide an email addresses for certbot admin contact, root alias, and catch-all to receive all forwarded emails from domain  )

       ansible-playbook  --user root -e "admin_email=<<certbot admin email address>> root_email_alias=<<email alias for root user>> forwarding_email=<<catch-all email for domain>>" -i inventory mail-send-only.yml


