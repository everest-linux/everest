Glacier is a simple package manager written in Shell.

It uses wget as a backend to fetch tarballs from the package repository.

It saves package information files to /etc/glacier/pkginfo

### Packaging

Packages should be formatted as `tar.gz` archives, and should contain the following:

- The package's executable (or any files required to compile said program)
- 3 instruction scripts written in Shell, INSTALL.sh, UPDATE.sh, and REMOVE.sh
- package_name-pkginfo.json, containing the following:
```
{
    "package_name": "NAME HERE",
    "package_version": "VERSION HERE",
    "package_description": "DESCRIPTION HERE",
    "src_tree_size": "SIZE OF SOURCE TREE HERE",
    "exec_size": "EXECUTABLE SIZE HERE",
    "license": "LICENSE NAME HERE",
}
```
All packages should be uploaded to https://github.com/everest-linux/glacier-pkgs by adding the package tarball to the pkgs folder, and submitting a pull request.
