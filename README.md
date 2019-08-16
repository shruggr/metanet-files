# metanet-files protocol

## FILE
1. META
1 .ID
1. PARENT_DIR || OP_0
1. VERSION
1. FILE
| Metadata MAP attributes

## BLOB
1. META
1. ID - repeated for each chunk
1. PARENT_FILE
1. SEQUENCE - must increase by 1 each chunk
1. BLOB - append to blob
1. <data>
1. START - *optional* start position in blob to replace
1. END - *optional* end position in blob to replace. If > 0, repace START - END with blob

## Dir
1. META
1. ID
1. PARENT_DIR || OP_0
1. VERSION
1. DIR
| Metadata MAP attributes

## REFERENCE
1. META
1. ID
1. PARENT_DIR || OP_0
1. VERSION
1. REF
1. <target node id>
1. <version id> - *optional* points to a specific version
| Metadata MAP attributes (referenced object metadata can be modified)
