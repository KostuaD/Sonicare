# Sonicare

# Philips Sonicare BLE controller for ESPHome
# (Updated: move on_boot under `esphome:` to avoid "Component not found: on_boot" error)
#
# Explanation of change:
# The previous placement of `on_boot:` at the very top-level caused ESPHome to treat it
# as a component name, producing "Component not found: on_boot". Placing `on_boot:` as a
# child of the `esphome:` section is the correct form for this ESPHome version.
#
# I only moved the on_boot block under the existing `esphome:` section and left the
# rest of your configuration intact. The on_boot actions ensure GPIO3 is driven LOW
# (enable RF switch control) and GPIO14 is set HIGH (external antenna) by default,
# and the global variable is updated accordingly.
#

Board ESP32-C6: https://wiki.seeedstudio.com/xiao_esp32c6_getting_started/

