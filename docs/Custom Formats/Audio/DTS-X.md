- HDBits labels DTS-X as DTS-HD MA 7.1 sometimes

```json
{
  "name": "DTS-X",
  "includeCustomFormatWhenRenaming": false,
  "specifications": [
    {
      "name": "DTS X",
      "implementation": "ReleaseTitleSpecification",
      "negate": false,
      "required": true,
      "fields": {
        "value": "\\b(dts[-_. ]?x)\\b(?!\\d)"
      }
    },
    {
      "name": "Not Basic DTS",
      "implementation": "ReleaseTitleSpecification",
      "negate": true,
      "required": true,
      "fields": {
        "value": "DTS[ .]?[1-9]"
      }
    },
    {
      "name": "Not Basic Dolby Digital",
      "implementation": "ReleaseTitleSpecification",
      "negate": true,
      "required": true,
      "fields": {
        "value": "\\bDD[^a-z+]|(?<!e)ac3"
      }
    },
    {
      "name": "Not Dolby Digital Plus",
      "implementation": "ReleaseTitleSpecification",
      "negate": true,
      "required": true,
      "fields": {
        "value": "\\bDD[P+]|\\b(e[-_. ]?ac3)\\b"
      }
    },
    {
      "name": "Not TrueHD/ATMOS",
      "implementation": "ReleaseTitleSpecification",
      "negate": true,
      "required": true,
      "fields": {
        "value": "True[ .-]?HD|\\bATMOS(\\b|\\d)"
      }
    },
    {
      "name": "Not FLAC",
      "implementation": "ReleaseTitleSpecification",
      "negate": true,
      "required": true,
      "fields": {
        "value": "\\bFLAC(\\b|\\d)"
      }
    },
    {
      "name": "Not AAC",
      "implementation": "ReleaseTitleSpecification",
      "negate": true,
      "required": true,
      "fields": {
        "value": "\\bAAC(\\b|\\d)"
      }
    },
    {
      "name": "Not PCM",
      "implementation": "ReleaseTitleSpecification",
      "negate": true,
      "required": true,
      "fields": {
        "value": "\\b(l?)PCM(\\b|\\d)"
      }
    }
  ]
}
```