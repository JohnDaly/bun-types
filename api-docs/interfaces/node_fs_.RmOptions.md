[bun-types](https://github.com/oven-sh/bun-types/blob/master/api-docs/README.md) / [Exports](https://github.com/oven-sh/bun-types/blob/master/api-docs/modules.md) / ["node:fs"](https://github.com/oven-sh/bun-types/blob/master/api-docs/modules/node_fs_.md) / RmOptions

# Interface: RmOptions

["node:fs"](https://github.com/oven-sh/bun-types/blob/master/api-docs/modules/node_fs_.md).RmOptions

## Table of contents

### Properties

- [force](https://github.com/oven-sh/bun-types/blob/master/api-docs/interfaces/node_fs_.RmOptions.md#force)
- [maxRetries](https://github.com/oven-sh/bun-types/blob/master/api-docs/interfaces/node_fs_.RmOptions.md#maxretries)
- [recursive](https://github.com/oven-sh/bun-types/blob/master/api-docs/interfaces/node_fs_.RmOptions.md#recursive)
- [retryDelay](https://github.com/oven-sh/bun-types/blob/master/api-docs/interfaces/node_fs_.RmOptions.md#retrydelay)

## Properties

### force

• `Optional` **force**: `boolean`

When `true`, exceptions will be ignored if `path` does not exist.

**`Default`**

false

___

### maxRetries

• `Optional` **maxRetries**: `number`

If an `EBUSY`, `EMFILE`, `ENFILE`, `ENOTEMPTY`, or
`EPERM` error is encountered, Node.js will retry the operation with a linear
backoff wait of `retryDelay` ms longer on each try. This option represents the
number of retries. This option is ignored if the `recursive` option is not
`true`.

**`Default`**

0

___

### recursive

• `Optional` **recursive**: `boolean`

If `true`, perform a recursive directory removal. In
recursive mode, operations are retried on failure.

**`Default`**

false

___

### retryDelay

• `Optional` **retryDelay**: `number`

The amount of time in milliseconds to wait between retries.
This option is ignored if the `recursive` option is not `true`.

**`Default`**

100