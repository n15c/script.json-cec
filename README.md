# Send HDMI CEC commands through Kodi's JSON-RPC.


Kodi addon allowing HDMI-CEC control via Kodi's JSON-RPC.

Requires at least Kodi 19 Matrix and currently supports latest version Kodi 20 Nexus.


## Installation

#### Zip

Download the project as Zip and rename it as script.json-cec.zip. Use the GUI interface to install it in Kodi.

#### Copying

Clone the project and copy it to Kodi's addons directory, example: ~/.kodi/addons/



## Accepted commands

* 'activate' - Wake up playing device via a CEC peripheral
* 'standby' - Put playing device on standby via a CEC peripheral
* 'toggle' - Toggle state of playing device via a CEC peripheral
* 'stop_and_standby' - Stop any playback and place the CEC peripheral on standby

#### Example JSON request:
```
http://localhost:8080/jsonrpc?request={"jsonrpc":"2.0","method":"Addons.ExecuteAddon","params":{"addonid":"script.json-cec","params":{"command":"activate"}},"id":1}
```

#### Example Curl Request

```
curl --header 'Content-Type: application/json' --data-binary '{"jsonrpc":"2.0","method":"Addons.ExecuteAddon","params":{"addonid":"script.json-cec","params":{"command":"activate"}},"id":1}' http://kodi/jsonrpc
```
