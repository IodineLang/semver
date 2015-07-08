# Semantic Versioning (`semver`)

[![ion install semver](https://img.shields.io/badge/ion%20install-semver-blue.svg)](https://github.com/IodineLang/Ion)
![version v0.1.0](https://img.shields.io/badge/version-v0.2.0-blue.svg)
![deps](https://img.shields.io/badge/dependencies-none-green.svg)

`semver` is a semantic versioning library for Iodine. It's extremely lightweight and you're encouraged to bundle it with your projects if that's convenient. 

## Features
- Can parse strings such as `v0.1.0-pre` to `versionMajor`, `versionMinor`, `versionPatch` and `versionTag` variables.
- Can convert three version integers and a tag to a semver string.

## Examples

    use semver;
    sv = semver.SemanticVersion ("v0.7.3-rc");
    print (sv.versionMajor);
    print (sv.versionMinor);
    print (sv.versionPatch);
    print (sv.versionTag);
    if (sv.isAlpha ()) {
        print ("Alpha (before v1)");
    }
    
> 0
>
> 7
>
> 3
>
> rc
>
> Alpha (before v1)

    use semver;
    sv = semver.SemanticVersion (0, 3, 4, "beta");
    print (sv.versionString);
    
> v0.3.4-beta
