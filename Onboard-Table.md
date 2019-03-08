# Onobarding mechanisms

There are a lot of them.  Scroll to the right if you need to.  The information in here needs more updating.


|  x1 | WPS | Simple Serial # | DPP | BRSKI w/pre-registration | BRSKI with POP no pre-registration | BRSKI / THREAD | OCF | Alljoyn | Bluetooth | EAP-NOOB | Intel SDO | 3G/4G/5G | LoRaWAN | Zigbee |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| Correct Network Selection | Beacon based on user action |   | Yes, based on "configurator" | Hunt | Hunt |   | SoftAP / Beacon | Yes | Via Manual Pairing | Hunt |    |  | | Hunt |
| Onboard without Internet Acces  | Yes | Yes | Yes | No | Yes | No | Yes | Yes | Yes | Yes | Yes | No | | |
| Proof of ownership | No | No | No | Yes when linked to sales or system integrators | Yes when linked to sales or system integrators | Yes when linked to sales or system integrators | Yes | Yes | No | No | Yes | | | No |
| Supply chain security | No | No | No | MASA can be linked to supply chain management tools |   | MASA can be linked to supply chain management tools | No | No | No | No |   | | | No |
| Hands free* | No | No | No | Yes when linked to sales or system integrators | No | Yes with a MASA | No | No | Not with proof of posession | No | Yes | Yes? | | Not securely |
| Security model | Presumption of no other announcements | no | Yes | Yes | Yes |   | Yes |   | No real PoP | Dynamic Code Gen | Yes | | | Pre-provisioned |
| Status | Std |   | Std | In stream | Beginning |   | Std | Std | Std | Beginning |   | | | Std |
| Key type | None | Ser # | Asym. | X.509 | X.509+private |   | Asym | Asym | Asym | Asym | Asym | | |
| Manufacturing complexity | Nvram | Serial# | Key+Label | Cert+Registration | Cert+label |   | Key+Label | Key+Label | Minimal | Dynamic Code Gen |   | SIM/SoftCIM | | Preconfiguration |
| Deployment Challenges | Not Secure | Not secure | No EAP linkage | Internet access | Scan required |   | Scan required and no EAP | No EAP linkage |   |   | SDO components | | | |
| Who Implements | Lots |   | HPE | Siemens, Cisco, Sandelmann  |   | Siemens, NXP, Sandelmann, SILABs |   |   | Everyone |   | Intel, ARM | | | Lots |
