# Ransomware Victim Files

This reposistory contains 1GB of files for ransomware to encrypt. They are
selected to represent the file types and sizes typically found on a NextCloud
instance.

All files are publicly redistributable because they are either Public Domain /
[CC0](https://creativecommons.org/publicdomain/zero/1.0/), or
[Wikipedia articles](https://en.wikipedia.org) which are covered by
[CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/) and provided
with appropriate attribution. A separate YAML file contains provenance
metadata for every victim file, except for ZIP and RAR files where the
provenance metadata for each archive member is almost always contained inside
the archive itself.

Please note that *all loose YAML files have to be removed* before actually
using this fileset for ransomware analysis. They would otherwise represent a
very unusual filetype, with a very unusual size distribution. (The YAML files
in ZIP and RAR archives are accounted for in the file size distribution and
should not be removed.)

# Usage

The victim files should be placed in the respective Windows directories for
the user running the ransomware sample. For user `cuckoo`, they should go to:

| directory | Windows path                |
|-----------|-----------------------------|
| Documents | `C:\Users\cuckoo\Documents` |
| Downloads | `C:\Users\cuckoo\Downloads` |
| Music     | `C:\Users\cuckoo\Music`     |
| Pictures  | `C:\Users\cuckoo\Pictures`  |
| Videos    | `C:\Users\cuckoo\Videos`    |

These paths are the default storage locations for the respective Windows
Explorer "Libraries", while "Downloads" is the default download folder.
That is, they represent a user just placing files where Windows suggests
placing them, and doing so without exception. Since Windows 7, these paths
are identical on localized copies of Windows – only the name displayed in
the UI is different.
