# Hackintosh-OpenCore-TravelMate-P276M
Hackintosh du Acer TravelMate P276M

<img src="/screenshot.png"/>

## Configuration

| Specifications | Details                                                  |
| ------------------- | ------------------------------------------- |
| Version OpenCore     | 0.9.3      					|
| Version macOS           | Monterey 12.6.6    		    |
| Version SMBIOS           | MacBookPro14,1    		    |
| CPU | Intel i5-4210U               |
| iGPU          | Intel HD Graphics 4400            |
| Audio          | Realtek ALC283 (ALCID=88)            |

## Comment fonctionne un hackintosh ?

Pour comprendre le fonctionnement d'un hackintosh et plus précisément du dossier "EFI", je vous invite à regarder [ma vidéo](https://youtu.be/Gaffvrc63jk) traitant du sujet.

## Mise à niveau vers Ventura

Les CPU/iGPU Haswell ne sont plus compatibles avec macOS Ventura.
Vous devrez donc désactiver le SIP (remplacer `NVRAM -> csr-active-config` 00000000 par 03080000) et patcher macOS avec [OpenCore Legacy Patcher](https://github.com/dortania/OpenCore-Legacy-Patcher).

## Ce qui fonctionne

- CPU / Accélération graphique (usurpation du HD 4600)
- Gestion de la luminosité (les boutons physiques ne fonctionnent pas)
- Ethernet (via le kext RTL8111)
- Audio (haut-parleurs et sortie casque)
- Ports USB et SD (le mappage a été fait)
- Microphone
- Webcam
- Trackpad et clavier

## Ce qui ne fonctionne pas

- Wi-Fi et bluetooth (la carte Qualcomm Atheros ne fonctionne pas, remplacé sur mon PC par une [Intel AC7260](https://www.amazon.fr/gp/product/B07R8J3ZK5))
- Sortie de veille (lorsque le capot est rabattu puis relevé, l'écran reste noir)
