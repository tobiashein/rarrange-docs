# Configuration

If not already present you can add an empty ignore file via 'Add -> RArrange Configuration File' in the context menu of the solution node in the Solution Explorer.

![Add ignore file](assets/addconfigurationfile.png)

## Structure

### General Settings

| Value             | Type                            | Description                                                                                                           |
|-------------------|---------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| AddHeaderRegion   | bool                            | Determines whether comments at the top a file should be wrapped in a region named _Header_.                           |
| AddCatchAllRegion | bool                            | Determines whether members not belonging to any group will be wrapped in a region named _Other_ at the end of a file. |
| EndOfLineType     | [EndOfLineType](#endoflinetype) | Sort by name in ascending order.                                                                                      |
| UseTabs           | bool                            | Determines whether tabs should be used instead of spaces for indentation.                                             |

#### EndOfLineType

| Value   | Description                           |
|---------|---------------------------------------|
| Default | The type is determined by the OS.     |
| CRLF    | Use _\r\n_ as end of line characters. |
| LF      | Use _\n_ as end of line character.   |
| CR      | Use _\r_ as end of line character.   |

### Groups

### Sorters

#### Sorter Types

| Value              | Notes |
|--------------------|-------|
| Class              |       |
| Constructor        |       |
| ConversionOperator |       |
| Delegate           |       |
| Destructor         |       |
| Enum               |       |
| Event              |       |
| EventField         |       |
| Field              | Fields sorted by the same sorter will be compressed, i.e. surrounding blank lines will be removed unless a field or its successor have documentation comments. |
| Indexer            |       |
| Interface          |       |
| Method             |       |
| NestedType         |       |
| Operator           |       |
| Property           |       |
| Struct             |       |
| Type               |       |

#### Access Modifiers

| Value             |
|-------------------|
| Public            |
| Protected         |
| Internal          |
| ProtectedInternal |
| Private           |
| PrivateProtected  |

#### Modifiers

#### Sort Order

| Value                    | Description                                                                                 |
|--------------------------|---------------------------------------------------------------------------------------------|
| NameAscending            | Sort by name in ascending order.                                                            |
| NameDescending           | Sort by name in descending order.                                                           |
| ParameterCountAscending  | Sort by parameter count in ascending order. Applicable to _Constructors_, _Methods_, etc..  |
| ParameterCountDescending | Sort by parameter count in descending order. Applicable to _Constructors_, _Methods_, etc.. |
| AccessModifierAscending  | Sort by access modifiers in ascending order (see [Access Modifiers](#access-modifiers)).    |
| AccessModifierDescending | Sort by access modifiers in descending order (see [Access Modifiers](#access-modifiers)).   |

## Examples

- [Basic Example](./configuration_example_basic.md)
- [Field Grouping](./configuration_example_fieldgrouping.md)
- [Method Grouping](./configuration_example_methodgrouping.md)

## See Also

- [Access Modifiers (C# Reference)](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/access-modifiers)
- [C# Keywords](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords)
