```json
{
  "name": "DTS-HD MA",
  "includeCustomFormatWhenRenaming": true,
  "specifications": [
    {
      "name": "DTS-HD MA",
      "implementation": "ReleaseTitleSpecification",
      "negate": false,
      "required": true,
      "fields": {
        "value": "\\b(dts[-_. ]?(ma|hd([-_. ]?ma)?|xll))\\b"
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
      "name": "Not Dolby Digital Plus",
      "implementation": "ReleaseTitleSpecification",
      "negate": true,
      "required": true,
      "fields": {
        "value": "\\bDD[P+]|\\b(e[-_. ]?ac3)\\b"
      }
    },
    {
      "name": "Not Basic Dolby Digital ",
      "implementation": "ReleaseTitleSpecification",
      "negate": true,
      "required": true,
      "fields": {
        "value": "\\bDD[^a-z+]|(?<!e)ac3"
      }
    },
    {
      "name": "Not DTS X",
      "implementation": "ReleaseTitleSpecification",
      "negate": true,
      "required": true,
      "fields": {
        "value": "\\b(dts[-_. ]?x)\\b(?!\\d)"
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
    },
    {
      "name": "Not DTS-HD HRA/ES",
      "implementation": "ReleaseTitleSpecification",
      "negate": true,
      "required": true,
      "fields": {
        "value": "dts[-. ]?(es|(hd[. ]?)?(hr|hi))"
      }
    }
  ]
}
```

