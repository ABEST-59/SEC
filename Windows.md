Disable protocole NTLM 
  - Info : https://www.it-connect.fr/comment-desactiver-le-protocole-ntlm-dans-un-domaine-active-directory/

Activer DNSSEC
  - Info : https://www.it-connect.fr/securite-du-dns-activer-dnssec-sur-une-zone-dns-active-directory/

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
       
Disable protocole LLMN
 - Info : https://www.it-connect.fr/active-directory-comment-et-pourquoi-desactiver-les-llmnr-et-netbios/
   - GPO:
        - Configuration ordinateur > Modèles d'administration > Réseau > Client DNS
        - Désactiver la résolution de noms multidiffusion
        - Active

Disable protocole NetBIOS 
 - Info : https://www.it-connect.fr/active-directory-comment-et-pourquoi-desactiver-les-llmnr-et-netbios/
 -   DHCP:
     - Accédez à votre étendue et cliquez sur "Options d'étendue"
     - Cliquez sur l'onglet "Avancé" présent dans la fenêtre "Options étendue".
     - Pour l'option "Classe de fournisseur", choisissez "Options Microsoft Windows 2000".
     - Cochez l'option "001 Option Microsoft de désactivation du NetBIOS" pour la configurer sur cette étendue
     - Attribuez la valeur "0x2" à cette option pour désactiver le NetBIOS.
  
  
