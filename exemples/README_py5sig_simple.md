py5sig - SBA signaling messages automation and SBI fuzzer
=========================================

<div style="display: flex; align-items: center; margin-bottom: 20px;"> <img src="https://www.sgdsn.gouv.fr/files/styles/ds_image_paragraphe/public/files/Notre_Organisation/logo_anssi.png" alt="Texte alternatif" width="50%"><div> <h2 style="margin: 0;">Agence Nationale de Sécurité des Systèmes d'Information</h2> <p style="margin: 0;">ANSSI</p> </div> </div>

![badge_repo](https://img.shields.io/badge/ANSSI--FR-py5sig-white?logo=opensourceinitiative&style=for-the-badge)
![badge_category_internal](https://img.shields.io/badge/Category-internal-lightgrey?style=for-the-badge)
[![badge_openness_A](https://img.shields.io/badge/Openness-A-blue?style=for-the-badge)](https://guides.data.gouv.fr/autres-ressources-utiles/codes-sources-du-secteur-public-lesquels-ouvrir-pourquoi-et-comment#clarifier-quels-degres-douverture-pour-les-codes-sources)

*For more information on the background of the project and the meaning of the badges, please see the [page dedicated to ANSSI's open source strategy](https://cyber.gouv.fr/open-source-lanssi).*

Introduction
------------
<span style="color:red">**The fuzzing feature of py5sig should never be conducted on production equipment or systems. 
This testing technique can cause unexpected behavior, system crashes, data corruption, or security vulnerabilities. 
Always perform fuzzing in a controlled, isolated environment to ensure the safety and stability of production systems.**</span>

py5sig is a specialized testing tool designed to automate 5G signaling messages and find bugs (security or others) in implementations.

Contributing
-----

See [CONTRIBUTING.md](CONTRIBUTING.md)


Setup
-----
py5sig is a python package. It requires at least Python 3.10. 

1. Create a virtual environment: `python3 -m venv py5sig-venv`
2. Activate your virtual environment: `. ./py5sig-venv/bin/activate`
3. Install py5sig from the project directory: `pip install .`

Options
--------------------

This section summarizes what you can do with py5sig.

It can :
- Act as a NFc
- Obtain JWT token and automate signaling messages
- Fuzz NRF, AMF, SMF, UDM and many others NF

Act as a NFc
-----------------------

 The general command usage is :
```commandline
 Usage: py5sig [OPTIONS] URL 
```
Where :
- **URL**: The server's hostname or IP address with http:// ;

*Example:* `http://f5.nrf.5gc.mnc093.mcc208.3gppnetwork.org`

Discover a SMF in the core network as an AMF
```bash
$ py5sig https://o5.nrf.5gc.mnc070.mcc999.3gppnetwork.org \ 
  --nfInstanceId 5ba18e25-da97-492f-8b54-49a2ed65895d \
  --nfType AMF \
  --targetNfType SMF \
  --target-request NRF \
  --discovery
```
The tool can also support stack using mTLS with paramaters `--ca-cert`, `--client-cert`, `--private-key`
Moreover, OAuth2.0 can be used in SBA for authorization, it possible to call `--scope` option to request JSON Web Tokens (JWT).
```bash
py5sig http://f5.amf.5gc.mnc093.mcc208.3gppnetwork.org --supi imsi-208930000000005 \
  --target-request AMF \
  --nfInstanceId 7eb89a1b-3177-420a-aad2-a6cc10f3d9ca \
  --nfType AMF \
  --targetNfType AMF \
  --scope "namf-loc namf-comm" \
  --ueContextTransferReason MOBI_REG_UE_VALIDATED \
  --nrf-fqdn http://f5.nrf.5gc.mnc093.mcc208.3gppnetwork.org 
```

Fuzzing an SBI interface
-----------------------

### Fuzzer options
A OpenAPI fuzzer based on 3.0 specs have been developed to generate json objects or body objects based on RequestBody 
parameters and paths. It uses 3GPP specs as yaml files.
- `--fuzzing`, `-f`: , Call the Fuzzer object to run py5sig in fuzzing mode

-  `--targetNfType`: specify the NF to fuzz, it will fuzz all the SBI interfaces for the NF

Fuzzing with py5sig can specifically target :

- Request Body and JSON data ;
- NAS stack of AMF and SMF network functions ;

To start fuzzing a SBI interface, you can call `nrf-fqdn` if the core network required OAuth2.0

```bash
$ py5sig http://f5.smf.5gc.mnc093.mcc208.3gppnetwork.org \
    --nfInstanceId 7eb89a1b-3177-420a-aad2-a6cc10f3d9ca \
    --nfType AMF \
    --targetNfType SMF \
    --fuzzing \
    --nrf-fqdn http://f5.nrf.5gc.mnc093.mcc208.3gppnetwork.org
```

Known limitations
---

###  Coverage of signaling messages
- py5sig does not cover all signaling messages in the SBI of differents network functions (NF)
- py5sig only support 3GPP R16 specs

### Coverage of fuzzer module
The fuzzer module cannot cover all the NF and their SBI interfaces.
It supports only AMF, SMF, NRF, UDM, UDR, AUSF, PCF, CHF and BSF

### HTTP verbs support
The fuzzer only support GET, DELETE, POST and PUT 

### Development
To develop in py5sig, install the package in editable mode

```bash
$ cd py5sig
$ pip install -e .
```

Licence
---
See [LICENSE.md](LICENSE.md)


    This program is free software; you can redistribute it and/or modify it under the terms of the GNU General Public License
    as published by the Free Software Foundation; version 2 of the License.

    This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

    You should have received a copy
