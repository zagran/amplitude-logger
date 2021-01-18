# amplitude-logger

![GitHub-issues](https://img.shields.io/github/issues/zagran/amplitude-logger)

Python client for Amplitude API v2 (https://developers.amplitude.com/docs/http-api-v2)

## Installation

```
pip install amplitude-logger
```

# Usage

## Amplitude API

1) Request your API key at https://developers.amplitude.com/

2) Use that token to initialize client:

```python
from amplitude import AmplitudeLogger
api_key = 'xxxxxxxxxxxxxxx'

amplitude_logger = AmplitudeLogger(api_key=api_key)

event_args = {
    "user_id": "USER_ID",
    "event_type": "Event Name",
    "event_properties": {"param": "value", "data": "value"},
}
event = amplitude_logger.create_event(**event_args)
amplitude_logger.log_event(event)
```
