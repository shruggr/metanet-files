# metanet-files protocol

## FILE
1. META
1. ID
1. PARENT_DIR_TX
1. FILE

|
Metadata MAP attributes

## BLOB
1. META
1. ID - repeated for each chunk
1. PARENT_FILE_TX
1. BLOB - append to blob
1. `sequence` - must increment by 1 for each chunk
1. `data`
1. START - *optional* start position in blob to replace
1. END - *optional* end position in blob to replace. If > 0, repace START - END with blob

## Dir
1. META
1. ID
1. PARENT_DIR || OP_0
1. DIR

|
Metadata MAP attributes

## REFERENCE
1. META
1. ID
1. PARENT_DIR || OP_0
1. REFT | REFN
1. `target node id` - For REFT, txId. For REFN, nodeId

|
Metadata MAP attributes (referenced object metadata can be modified)

## Metadata
1. META
1. ID
1. PARENT
1. `MAP protocol id`

MAP attributes
