## What are Atomic variables?
This is lock free structures which use machine commands to ensure atomicity of operation.

Advice is to prefer atomic classes over locks in case you just have to change a single mutable variable concurrently.

