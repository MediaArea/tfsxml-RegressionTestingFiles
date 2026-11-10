Test files of tfsxml
====================

All the files in this directory were written for this test suite (synthetic
content, values are invented), they contain no third-party content.
They are dedicated to the public domain (CC0 1.0).

Each NAME.xml file has its expected trace in NAME.xml.txt.
Files must not be modified by tools changing line endings (see .gitattributes).

Directories:
- Basic: elements, attributes, text
- CData: CDATA sections
- Comment: comments
- Depth: more than 255 levels
- Entity: entities and character references
- Formats: synthetic files similar to real formats parsed by MediaInfoLib
  (ADM, S-ADM, XMP, MPEG-DASH, TTML, HDR Vivid)
- Malformed: truncated or incorrect content
- Prolog: BOM, XML declaration, DOCTYPE, content before and after the root
- Regression: issues found by fuzzing or reported
- Stream: content for testing data provided in chunks
- Unicode: non ASCII names and content
- Whitespace: CR, LF, tabs, spaces at various places

See Source/Doc/RegressionTest.md of tfsxml for the trace format and the protocol.
