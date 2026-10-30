# Home Assistant - конфиг HA Yellow (Kolossi)

YAML-конфиг Home Assistant: `configuration.yaml`, `packages/`, `blueprints/`,
`automations.yaml`, `scripts.yaml`, `scenes.yaml`, `go2rtc.yaml`.

Коммитит и пушит приложение Filesystem MCP на самом Yellow
(`/addons/filesystem_mcp`): Claude - осмысленными коммитами после правок,
плюс автокоммит раз в час для изменений из UI.

Что попадает в репо - белый список в `.gitignore`. Не попадают: `secrets.yaml`,
`.storage/`, база recorder, `zigbee2mqtt/`, `esphome/`, всё от HACS.
