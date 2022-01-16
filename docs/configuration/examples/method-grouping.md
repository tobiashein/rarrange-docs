# Method Grouping

The following configuration will group all methods in a region named _Methods_. The methods are then grouped into named regions according to their access modifiers.

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
      "regionName": "Methods",
      "groups": [
        {
          "regionName": "Public Methods",
          "sorters": [
            {
              "type": "method",
              "accessModifiers": [
                "public",
              ],
              "sortOrder": [
                "nameAscending"
              ]
            }
          ]
        },
        {
          "regionName": "Protected Methods",
          "sorters": [
            {
              "type": "method",
              "accessModifiers": [
                "protected"
              ],
              "sortOrder": [
                "nameAscending"
              ]
            }
          ]
        },
        {
          "regionName": "Private Methods",
          "sorters": [
            {
              "type": "method",
              "accessModifiers": [
                "private"
              ],
              "sortOrder": [
                "nameAscending"
              ]
            }
          ]
        },
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
        #region Methods

        #region Public Methods

        public void PublicMethodA() { }

        public void PublicMethodB() { }

        public void PublicMethodC() { }

        #endregion Public Methods

        #region Protected Methods

        protected void ProtectedMethodA() { }

        protected void ProtectedMethodB() { }

        protected void ProtectedMethodC() { }

        #endregion Protected Methods

        #region Private Methods

        private void PrivateMethodA() { }

        private void PrivateMethodB() { }

        private void PrivateMethodC() { }

        #endregion Private Methods

        #endregion Methods
    }
} 
```
