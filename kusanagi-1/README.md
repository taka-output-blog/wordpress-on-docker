```
sudo sed -e "s/{domain}/mydomain.com/g" \
         -e "s/{E-MAIL}/e-mail@mydomain.com/g" docker-compose.yml.template > docker-compose.yml
```
