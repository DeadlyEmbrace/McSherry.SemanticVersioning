# `VersionRange` class

```c#
[Serializable]
[CLSCompliant(true)]
public sealed class VersionRange
```

**Namespace:** [`McSherry.SemanticVersioning.Ranges`][1]  
**Minimum Version:** 1.1.0

Represents a range of acceptable versions. This class cannot be
inherited.

[1]: ../


## Constructors

- **[VersionRange(String)][2]**  
  Creates a version range from a string representing the range.
  
[2]: ./ctor(String).md


## Instance Methods

- **[SatisfiedBy(SemanticVersion)][3]**  
  Determines whether the current version range is satisfied by
  a specified [SemanticVersion][4].
- **[SatisfiedBy(SemanticVersion[])][5]**  
  Determines whether the current range is satisfied by all
  specified [SemanticVersion][4] instances.
  
[3]: ./SatisfiedBy(SemanticVersion).md
[4]: ../SemanticVersion
[5]: ./SatisfiedBy(SemanticVersion[]).md


## Static Methods

- **[Parse(String)][6]**  
  Parses a version range from a string.
- **[TryParse(String, out SemanticVersion)][7]**  
  Attempts to parse a version range from a string.
  
[6]: ./Parse(String).md
[7]: ./TryParse(String,VersionRange).md


## Remarks

A version range specifies a set of semantic versions that are
acceptable, and is used to check that a given semantic version
fits within this set.

Version ranges use the [`node-semver`][8] syntax for ranges.
Specifically, ranges are based on the specification as it was
written for the [`v5.0.0`][9] release of `node-semver`.

Presently, only the basic range syntax is supported.

[8]: https://github.com/npm/node-semver
[9]: https://github.com/npm/node-semver/blob/v5.0.0/README.md#ranges