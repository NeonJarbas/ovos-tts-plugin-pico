## Description

OpenVoiceOS TTS plugin for [PicoTTS](https://github.com/naggety/picotts)

## Install

```bash
pip install jarbas_plugin_pico_tts
```

`pico2wave` needs to be available, in a pi this can be installed with

```bash
apt-get install libttspico0
apt-get install libttspico-utils
```

you can also install from [source](https://github.com/naggety/picotts)


## Configuration


```json
  "tts": {
    "module": "pico_tts_plugin"
 }
```

the Voice corresponds to a language code, it should be auto detected from global config

you can also set it explicitly to one of `"de-DE", "es-ES", "fr-FR", "it-IT", "en-US"`


```json
  "tts": {
    "module": "pico_tts_plugin",
    "pico_tts_plugin": {
      "voice": "en-US"
    }
 }
```
