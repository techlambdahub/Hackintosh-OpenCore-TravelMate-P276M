# Hackintosh-OpenCore-TravelMate-P276M
Hackintosh du Acer TravelMate P276M

<img src="/screenshot.png"/>

## 💻 Configuration

| Specifications | Details                                                  |
| ------------------- | ------------------------------------------- |
| Version OpenCore     | 0.9.3      					|
| CPU | Intel i5-4210U               |
| iGPU          | Intel HD Graphics 4400            |
| Audio          | Realtek ALC283 (ALCID=88)            |

## 🍎 Comment fonctionne un hackintosh ?

Pour comprendre le fonctionnement d'un hackintosh et plus précisément du dossier "EFI", je vous invite à regarder [ma vidéo](https://youtu.be/Gaffvrc63jk) traitant du sujet.

## 📂 Variants

Cette archive contient deux dossiers EFI :
| Specifications | Monterey and older                                                  | Ventura and newer                                                  |
| ------------------- | ------------------------------------------- | ------------------------------------------- |
| Version max     | Monterey 12      					| Current (Sonoma 14)      					|
| SMBIOS | MacBookPro12,1               | MacBookPro15,2               |
| SIP          | Enabled `00000000`            | Semi-enabled `03080000`            |
| Boot-args          | -            | `amfi_get_out_of_my_way=0x1`            |

Le dossier `Monterey and older` ne nécessite pas d'[OpenCore Legacy Patcher](https://github.com/dortania/OpenCore-Legacy-Patcher) comparé au second.

## ✅ Ce qui fonctionne

- CPU / Accélération graphique (usurpation du HD 4600)
- Gestion de la luminosité (les boutons physiques ne fonctionnent pas)
- Ethernet (via le kext RTL8111)
- Audio (haut-parleurs et sortie casque)
- Ports USB et SD (le mappage a été fait)
- Microphone
- Webcam
- Trackpad et clavier

## ❌ Ce qui ne fonctionne pas

- Wi-Fi et bluetooth (la carte Qualcomm Atheros ne fonctionne pas, remplacé sur mon PC par une [Intel AC7260](https://www.amazon.fr/gp/product/B07R8J3ZK5))
- Sortie de veille (lorsque le capot est rabattu puis relevé, l'écran reste noir ou le PC redémarre)
