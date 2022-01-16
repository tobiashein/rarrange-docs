# Sorters

## Sorter Types

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

## Access Modifiers

| Value             |
|-------------------|
| Public            |
| Protected         |
| Internal          |
| ProtectedInternal |
| Private           |
| PrivateProtected  |

## Modifiers

## Sort Order

| Value                    | Description                                                                                 |
|--------------------------|---------------------------------------------------------------------------------------------|
| NameAscending            | Sort by name in ascending order.                                                            |
| NameDescending           | Sort by name in descending order.                                                           |
| ParameterCountAscending  | Sort by parameter count in ascending order. Applicable to _Constructors_, _Methods_, etc..  |
| ParameterCountDescending | Sort by parameter count in descending order. Applicable to _Constructors_, _Methods_, etc.. |
| AccessModifierAscending  | Sort by access modifiers in ascending order (see [Access Modifiers](#access-modifiers)).    |
| AccessModifierDescending | Sort by access modifiers in descending order (see [Access Modifiers](#access-modifiers)).   |
