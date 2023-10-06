```json
{
  "name": "HDR10+",
  "includeCustomFormatWhenRenaming": false,
  "specifications": [
    {
      "name": "HDR10+",
      "implementation": "ReleaseTitleSpecification",
      "negate": false,
      "required": true,
      "fields": {
        "value": "\\bHDR10(\\+|P(lus)?\\b)"
      }
    },
    {
      "name": "Not PQ",
      "implementation": "ReleaseTitleSpecification",
      "negate": true,
      "required": true,
      "fields": {
        "value": "\\b(PQ)\\b"
      }
    },
    {
      "name": "Not HLG",
      "implementation": "ReleaseTitleSpecification",
      "negate": true,
      "required": true,
      "fields": {
        "value": "\\b(HLG)\\b"
      }
    },
    {
      "name": "Not SDR",
      "implementation": "ReleaseTitleSpecification",
      "negate": true,
      "required": true,
      "fields": {
        "value": "\\bSDR(\\b|\\d)"
      }
    }
  ]
}
```

