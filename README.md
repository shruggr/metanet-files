# metanet-files protocol

## 
META
ID
PARENT_DIR || OP_0
VERSION
FILE
| Metadata MAP attributes

## Blob
Append to Blob
META
ID - repeated for each chunk
PARENT_FILE
SEQUENCE - must increase by 1 each chunk
BLOB - append to blob
<data>
START - *optional* start position in blob to replace
END - *optional* end position in blob to replace

## Dir
META
ID
PARENT_DIR || OP_0
VERSION
DIR
| Metadata MAP attributes

## REFERENCE
META
ID
PARENT_DIR || OP_0
VERSION
REF | REFV
<target node id>
<version id> - for REFV, points to a specific version
| Metadata MAP attributes (referenced object metadata can be modified)
