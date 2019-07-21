```
sudo sed -e "s/{database_root_password}/database_root_password/g" \
         -e "s/{database_user_name}/database_user_name/g" \
         -e "s/{database_password}/database_password/g" \
         -e "s/{database_name}/wordpress/g" docker-compose.yml.template > docker-compose.yml
```
