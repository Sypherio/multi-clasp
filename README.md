multi-clasp
===========

`multi-clasp` is meant to solve a specific problem:
You have multiple google artifacts (sheets, docs, etc.) that all use the same Apps Script project.

You want them to share the same code, but making this Apps Script project into a library significantly slows its performance.

The solution is to maintain a reference to each artifact's Apps Script project, and simultaneously push changes to these projects so they can receive updates while maintaining their non-library performance.

### Example File

Create a .multi-clasp.json file, which is just an array of JSON objects identical to the standard .clasp.json format.

You do not need a .clasp.json file anymore.

```
[
	{
		"scriptId": "1VBe_bo7OtOw1EQ_f86HBKSDEDdcGX3mYfCNIcp5L2tR1P-VAU8Sl7KX1",
		"rootDir": "build"
	},
	{
		"scriptId": "1VBe_bo7OtOw1EQ_f86HBKSDEDdcGX3mYfCNIcp5L2tR1P-VAU8Sl7KX2",
		"rootDir": "build"
	},
	{
		"scriptId": "1VBe_bo7OtOw1EQ_f86HBKSDEDdcGX3mYfCNIcp5L2tR1P-VAU8Sl7KX3",
		"rootDir": "build"
	}
]
```

### Usage

`multi-clasp push`