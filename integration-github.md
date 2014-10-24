# Intégration avec Github

Plugins : 
* GitHub plugin (pouvoir déclencer des jobs sur des Pulls)
* GitHub Authentification Plugins (pouvoir se connecter à Jenkins avec son compte GitHub)

## GitHub Authentification

1 - Créer une nouvelle application sur `https://github.com/settings/applications`
Settings : 
Url : http://myserver.com:8080/
Callback : http://myserver.com:8080/securityRealm/finishLogin
