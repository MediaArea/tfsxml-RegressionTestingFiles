Test files of the tinyxml2 compatibility layer of tfsxml
========================================================

All the files in this directory were written for this test suite (synthetic
content), they contain no third-party content.
They are dedicated to the public domain (CC0 1.0).

Each NAME.xml file has its expected results in NAME.xml.txt (dump of the
results of the API with 5 parsing options, see RegressionTest_TinyXml2.h of
tfsxml). The expected results were checked against tinyxml2 6.2.0.
Files must not be modified by tools changing line endings (see .gitattributes).

The first part of the name is the tested part of the parsing: Attribute, Cdata,
Comment, Declaration, Depth (nesting depth limit), Doctype, Document (content
before and after the root, empty documents...), Format (samples of formats read
with tinyxml2 in MediaInfoLib), Incomplete (truncated content), Reference
(entities and character references), Tag, Text.

See Source/Doc/RegressionTest.md of tfsxml for the protocol.
