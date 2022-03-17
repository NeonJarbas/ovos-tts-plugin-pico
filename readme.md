## Description

OpenVoiceOS TTS plugin for [PicoTTS](https://github.com/naggety/picotts)

## Install

```bash
pip install ovos-tts-plugin-pico
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
    "module": "ovos-tts-plugin-pico"
 }
```

the Voice corresponds to a language code, it should be auto detected from global config

you can also set it explicitly to one of `"de-DE", "es-ES", "fr-FR", "it-IT", "en-US"`


```json
  "tts": {
    "module": "ovos-tts-plugin-pico",
    "ovos-tts-plugin-pico": {
      "voice": "en-US"
    }
 }
```


## Docker

build it
```bash
docker build . -t ovos/pico
```

run it
```bash
docker run -p 8080:9666 ovos/pico
```

use it `http://localhost:8080/synthesize/hello`