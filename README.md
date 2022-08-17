# WebSweeper

WebSweeper is a web scale batch processing framework oriented at low performance distributed computing systems.

![Network and processing diagram](https://i.imgur.com/7SDoNQU.png)

The mainstay of the framework is orienting the processing flow into micro and macro batches

Micro batches are small processing steps that are purely computational in their core(Strictly no I/O within)

Macro batches are a wrapper for chains of micro batches that deal with I/O and joining data coming in from other batches

## Current limitations:

1. This is a purely forward procesing framework. The whole flow must be completed regardless of what was queried.
2. Requires a powerful central scheduler to shard workloads and join final data.
3. Primitive scheduler. Sharding, error handling and final processing are custom written for each workflow.
