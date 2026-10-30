Придумай схему для автоматизации света в следующих комнатах.

Требования:
 - Свет должен включаться, если в комнате кто-то есть и текущего освещения недостаточно
 - Свет должен выключаться, если в комнате никого нет
 - Свет не должен включаться, если в комнате кто-то есть и он мануально выключил свет
 - Необходимо учесть edge-кейсы: если в комнате кто-то есть, было достаточно света, но стало недостаточно, то свет должен включиться
 - На выходе должны быть как минимум две автоматизации, чтобы их можно было отключить при необходимости:
 	- automation.lights_living_room
 	- automation.lights_semyons_bedroom
- Использовать дополнительные helpers (например, `input_boolean.living_room_manual_off`) - нельзя.
  Для этих целей может служить статус самой автоматизации. Однако можно делать дополнительные автомаитизации:
  	вроде, Lights Turn Off и Lights Lockout.

# Living Room (тут 3 триггера, т.к. 3 света)
- binary_sensor.living_room_dining_area_occupancy
- binary_sensor.living_room_bright (device_class: light)
- light.living_room_dining_area

- binary_sensor.living_room_sofa_occupancy
- binary_sensor.living_room_bright (device_class: light)
- light.living_room_sofa

- binary_sensor.living_room_tv_area_occupancy
- binary_sensor.living_room_bright (device_class: light)
- light.living_room_tv_area

# Semyon's Bedroom
- binary_sensor.semyons_bedroom_occupancy
- binary_sensor.semyons_bedroom_bright (device_class: light)
- light.semyons_bedroom + light.semyons_bedside_lamp
