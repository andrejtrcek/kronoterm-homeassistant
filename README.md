# kronoterm-homeassistant
Home Assistant YAML koda za pridobivanje podatkov in krmiljenje Kronoterm / Termotehnika toplotne črpalke. Za delovanje potrebujete le RS485 Wifi ali Ethernet modul, ki je dostopen z Home assistant strežnika. Pridobivanje podatkov in krmiljenje se izvaja neposredno s Home assistant strežnika.

# Postopek vzpostavitve povezave
Pridobivanje podatkov in krmiljenje Kronoterm (Termotehnika) toplotne črpalke se izvaja preko RS485 - ethernet modula ([primer modula](https://www.aliexpress.com/item/1005006965738494.html)), ki ga povežete s TEX vhodom na toplotni črpalki ([navodila za priklop](https://github.com/user-attachments/files/17962067/22-16-17-4021-05_Modbus_BMS_TT3000web.pdf)).

# Kako uporabiti YAML?
- **configuration.yaml** - kodo kopirate v obstoječo **configuration.yaml**. Na vrhu dodate še naslednjo kodo, s katero boste vključili tudi **modbus** in **template** nastavitve:
- 
**modbus: !include kronoterm-modbus.yaml
template: !include kronoterm-template.yaml**

- **kronoterm-modbus.yaml** - datoteko kopirate v **/homeassistant/kronoterm-modbus.yaml** in vpišete IP vašega RS485 TCP strežnika (3. vrstica - zamenjate **[IP ADDRESS]**)
- **kronoterm-template.yaml** - datoteko kopirate v **/homeassistant/kronoterm-template.yaml**
- **kronoterm-lovelace.yaml** - na prvi strani Home assistant dodate novo kartico - izberete "Ročno" oz. "Custom", kopirate kodo iz **kronoterm-lovelace.yaml** v novo kartico in shranite

# Splošni pogoji
Uporaba kode na lastno odgovornost. Za uporabo kode ali morebitne posledice uporabe ne prevzemam nobene odgovornosti.
