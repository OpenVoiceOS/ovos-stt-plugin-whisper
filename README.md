## Description

This is an OpenVoiceOS STT plugin for [Whisper](https://github.com/guillaumekln/faster-whisper). It uses the `transformers` library to run the model.

## Install

`pip install ovos-stt-plugin-whisper`

## Configuration

This example uses the large model with a GPU.

```json
  "stt": {
    "module": "ovos-stt-plugin-whisper",
    "ovos-stt-plugin-whisper": {
        "model": "openai/whisper-large-v3",
        "use_cuda": true
    }
  }
```

You can also pass the full path to a local model, or any Hugging Face `repo_id`, for example `"projecte-aina/whisper-large-v3-ca-3catparla"`.

## Related projects

- [OpenVoiceOS/ovos-plugin-manager](https://github.com/OpenVoiceOS/ovos-plugin-manager): the plugin manager that loads this STT plugin.
- [OpenVoiceOS/ovos-stt-plugin-whispercpp](https://github.com/OpenVoiceOS/ovos-stt-plugin-whispercpp): a sibling plugin that runs Whisper with `whisper.cpp`.
- [OpenVoiceOS/ovos-stt-plugin-whisper-lm](https://github.com/OpenVoiceOS/ovos-stt-plugin-whisper-lm): a sibling plugin that adds language-model rescoring to Whisper.
