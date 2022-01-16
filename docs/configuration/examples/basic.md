# Basic Example

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
      "regionName": "Constructors",
      "sorters": [
        {
          "type": "constructor",
          "sortOrder": [
            "accessModifierAscending",
            "nameAscending"
          ]
        }
      ]
    },
    {
      "regionName": "Fields",
      "sorters": [
        {
          "type": "field",
          "sortOrder": [
            "accessModifierAscending",
            "nameAscending"
          ]
        }
      ]
    },
    {
      "regionName": "Properties",
      "sorters": [
        {
          "type": "property",
          "sortOrder": [
            "accessModifierAscending",
            "nameAscending"
          ]
        }
      ]
    },
    {
      "regionName": "Methods",
      "sorters": [
        {
          "type": "method",
          "sortOrder": [
            "accessModifierAscending",
            "nameAscending"
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
    public class Person
    {
        #region Constructors

        public Person(bool isActive, string givenName, string familyName)
        {
            _isActive = isActive;

            GivenName = givenName;
            FamilyName = familyName;
        }

        #endregion Constructors

        #region Fields

        private readonly bool _isActive;

        #endregion Fields

        #region Properties

        public string FamilyName { get; set; }

        public string GivenName { get; set; }

        #endregion Properties

        #region Methods

        public string GetFullName() => $"{GivenName} {FamilyName}";

        #endregion Methods
    }
} 
```