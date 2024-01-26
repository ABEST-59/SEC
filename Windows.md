Disable protocole mDNS
  - Info : https://www.it-connect.fr/active-directory-desactiver-le-protocole-mdns-windows/
      - GPO:
        - Configuration ordinateur > Préférences > Paramètres Windows > Registre
        - Action : Mettre à jour (même si cette valeur n'existe pas par défaut)
        - Ruche : HKEY_LOCAL_MACHINE
        - Chemin d'accès de la clé : SYSTEM\CurrentControlSet\Services\Dnscache\Parameters
        - Nom de valeur : EnableMDNS
        - Type de valeur : REG_DWORD
        - Données de valeur : 0
       
