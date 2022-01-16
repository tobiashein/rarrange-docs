# General Settings

| Value             | Type                            | Description                                                                                                           |
|-------------------|---------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| AddHeaderRegion   | bool                            | Determines whether comments at the top a file should be wrapped in a region named _Header_.                           |
| AddCatchAllRegion | bool                            | Determines whether members not belonging to any group will be wrapped in a region named _Other_ at the end of a file. |
| EndOfLineType     | [EndOfLineType](#endoflinetype) | Sort by name in ascending order.                                                                                      |
| UseTabs           | bool                            | Determines whether tabs should be used instead of spaces for indentation.                                             |

## EndOfLineType

| Value   | Description                           |
|---------|---------------------------------------|
| Default | The type is determined by the OS.     |
| CRLF    | Use _\r\n_ as end of line characters. |
| LF      | Use _\n_ as end of line character.   |
| CR      | Use _\r_ as end of line character.   |