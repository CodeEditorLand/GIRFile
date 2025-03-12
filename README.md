# gir-files

This repository contains the
[GIR](https://developer.gnome.org/programming-guidelines/stable/introspection.html.en)
files used to generate all [`gtk-rs`](https://github.com/gtk-rs/gtk-rs) crates.

## Updating all files

You can update all the files by doing:

```console
$ ./dl.sh
```

This command will fetch the gir files for the latest release of each library.
When updating all files, make sure you do not inadvertedly overwrite gir files
which were manually updated and which have not yet been included in a release of
the corresponding library.

## Updating a gir file manually

In general we prefer to use gir files that have been included in a release,
however sometimes it is required to update a specific gir files to incorporate a
bug fix or a missing API.

Manually copy the updated gir file and then run

```console
$ ./reformat.sh
$ ./fix.sh
```

## Validating an update

After updating the gir files, please don't forget to check that
[`gir`](https://github.com/gtk-rs/gir) can still run with the new files and that
the generated files have no breaking changes.

Refer to the [`gtk-rs`](https://github.com/gtk-rs/gtk-rs) README file for
further information about regenerating the `gtk-rs` crates.

## Funding

This project is funded through
[NGI0 Commons Fund](https://nlnet.nl/commonsfund), a fund established by
[NLnet](https://nlnet.nl) with financial support from the European Commission's
[Next Generation Internet](https://ngi.eu) program. Learn more at the
[NLnet project page](https://nlnet.nl/project/Land).

| Land                                                                                                                                                   | PlayForm                                                                                                                                                    | NLNET                                                                                         | NGI0 Commons Fund                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| [<img src="https://raw.githubusercontent.com/CodeEditorLand/Asset/refs/heads/Current/Logo/Land.svg" height="80px" alt="Land"  />](https://editor.land) | [<img src="https://raw.githubusercontent.com/PlayForm/Asset/refs/heads/Current/Logo/PlayForm.svg" height="80px" alt="PlayForm"  />](https://playform.cloud) | [<img width="240px" src="https://nlnet.nl/logo/banner.svg" alt="NLNET"  />](https://nlnet.nl) | [<img width="240px" src="https://nlnet.nl/image/logos/NGI0CommonsFund_tag_black_mono.svg" alt="NGI0 Commons Fund"  />](https://nlnet.nl/commonsfund) |
