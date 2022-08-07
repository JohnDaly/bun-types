[bun-types](https://oven-sh.github.io/bun-types/README.md) / [Exports](https://oven-sh.github.io/bun-types/modules.md) / QueuingStrategyInit

# Interface: QueuingStrategyInit

## Table of contents

### Properties

- [highWaterMark](https://oven-sh.github.io/bun-types/interfaces/QueuingStrategyInit.md#highwatermark)

## Properties

### highWaterMark

• **highWaterMark**: `number`

Creates a new ByteLengthQueuingStrategy with the provided high water mark.

Note that the provided high water mark will not be validated ahead of time. Instead, if it is negative, NaN, or not a number, the resulting ByteLengthQueuingStrategy will cause the corresponding stream constructor to throw.
