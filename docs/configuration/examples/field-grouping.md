# Field Grouping

The following configuration will group all private fields with optional modifiers _readonly_ and _static_ in a region named _Fields_. All fields sorted by the same sorter are _compressed_, i.e. their surrounding blank lines are removed unless they or their successor have documentation comments.

## Configuration

```json
{
  "$schema": "https://raw.githubusercontent.com/tobiashein/rarrange.schema/develop/rarrange.schema.json",
  "catchAllRegion": true,
  "endOfLineType": "default",
  "headerRegion": true,
  "tabs": false,
  "groups": [
    {
      "regionName": "Fields",
      "groups": [
        {
          "sorters": [
            {
              "type": "field",
              "accessModifiers": [
                "private"
              ],
              "modifiers": [
                "readonly"
              ],
              "sortOrder": [
                "nameAscending"
              ]
            }
          ]
        },
        {
          "sorters": [
            {
              "type": "field",
              "accessModifiers": [
                "private"
              ],
              "modifiers": [
                "static"
              ],
              "sortOrder": [
                "nameAscending"
              ]
            }
          ]
        },
        {
          "sorters": [
            {
              "type": "field",
              "accessModifiers": [
                "private"
              ],
              "sortOrder": [
                "nameAscending"
              ]
            }
          ]
        }
      ]
    }
  ]
}
```

## Result

```csharp
namespace MyApplication
{
    public class Fields
    {
        #region Fields

        private readonly object _privateReadOnlyFieldA;
        private readonly object _privateReadOnlyFieldB;
        private readonly object _privateReadOnlyFieldC;

        private static object _privateStaticFieldA;

        /// <summary>
        /// Documentation comment.
        /// </summary>
        private static object _privateStaticFieldB;

        private static object _privateStaticFieldC;

        private object _privateFieldA;
        private object _privateFieldB;

        /// <summary>
        /// Documentation comment.
        /// </summary>
        private object _privateFieldC;

        #endregion Fields
    }
}
```
