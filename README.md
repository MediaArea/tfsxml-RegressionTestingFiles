# tfsxml-RegressionTestingFiles

Test files of [tfsxml](https://github.com/MediaArea/tfsxml), the Tiny Fast
Streamable XML parser.

- `Files`: XML files with their expected traces (`NAME.xml.txt`), for the
  `RegressionTest` tool of tfsxml and as seed corpus for fuzzing, see
  [Files/ReadMe.txt](Files/ReadMe.txt) for the content.
- `TinyXml2`: XML files with the expected results of the tinyxml2
  compatibility layer of tfsxml (`NAME.xml.txt`), for the
  `RegressionTest_TinyXml2` tool and as seed corpus for its fuzzing, see
  [TinyXml2/ReadMe.txt](TinyXml2/ReadMe.txt).

All the files were written for the test suite, they contain no third-party
content and are dedicated to the public domain (CC0 1.0).

## Usage

The builds of tfsxml look for this repository next to the tfsxml directory:
```sh
git clone https://github.com/MediaArea/tfsxml.git
git clone https://github.com/MediaArea/tfsxml-RegressionTestingFiles.git
```

Another location can be set with `-DTFSXML_TESTING_FILES=DIR` (CMake) or with
the `TFSXML_TESTING_FILES` environment variable (`make check` of the GNU
autotools build).

## Changes

Files are compared byte per byte, line endings included (see `.gitattributes`).

After adding a test file, generate its expected trace with
`RegressionTest --update` (`RegressionTest_TinyXml2 --update` in `TinyXml2`)
and check it by reading it, see the
[regression test protocol](https://github.com/MediaArea/tfsxml/blob/main/Source/Doc/RegressionTest.md).

A change of the behavior of tfsxml comes with updated expected traces here, in
a branch having the same name in both repositories: the CI of tfsxml uses the
branch with the same name in the fork of this repository of the author of the
change if it exists, else the main branch.
