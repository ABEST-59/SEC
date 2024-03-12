- REF: https://www.cisecurity.org/cis-benchmarks
- Windows
  - HardeningKitty
    -  Info : https://www.it-connect.fr/hardening-securite-windows-et-windows-server-avec-hardeningkitty/#C_Auditer_la_configuration_de_la_machine
    -  Git: https://github.com/scipag/HardeningKitty
      - # Audit des paramètres machine
        Invoke-HardeningKitty -Mode Audit -Log -Report -FileFindingList ".\lists\finding_list_cis_microsoft_windows_server_2022_22h2_2.0.0_machine.csv"
        # Audit des paramètres utilisateur
        Invoke-HardeningKitty -Mode Audit -Log -Report -FileFindingList ".\lists\finding_list_cis_microsoft_windows_server_2022_22h2_2.0.0_machine.csv"
      
