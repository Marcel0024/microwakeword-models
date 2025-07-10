### Example .yaml file

```yaml
substitutions:
  name: home-assistant-voice-093bb2
  friendly_name: Coco
packages:
  Nabu Casa.Home Assistant Voice PE: github://esphome/home-assistant-voice-pe/home-assistant-voice.yaml
esphome:
  name: ${name}
  name_add_mac_suffix: false
  friendly_name: ${friendly_name}
api:
  encryption:
    key: /REDACTED/

micro_wake_word:
  models:
    - model: "https://raw.githubusercontent.com/Marcel0024/microwakeword-models/refs/heads/main/hey_dushi.json"
      id: hey_dushi   
    - model: "https://raw.githubusercontent.com/Marcel0024/microwakeword-models/refs/heads/main/hey_coco.json"
      id: coco
    - model: "https://raw.githubusercontent.com/Marcel0024/microwakeword-models/refs/heads/main/coco.json"
      id: hey_coco

wifi:
  ssid: !secret wifi_ssid
  password: !secret wifi_password
```
