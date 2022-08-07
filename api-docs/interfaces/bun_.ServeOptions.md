[bun-types](https://github.com/oven-sh/bun-types/blob/master/api-docs/README.md) / [Exports](https://github.com/oven-sh/bun-types/blob/master/api-docs/modules.md) / ["bun"](https://github.com/oven-sh/bun-types/blob/master/api-docs/modules/bun_.md) / ServeOptions

# Interface: ServeOptions

["bun"](https://github.com/oven-sh/bun-types/blob/master/api-docs/modules/bun_.md).ServeOptions

## Table of contents

### Properties

- [baseURI](https://github.com/oven-sh/bun-types/blob/master/api-docs/interfaces/bun_.ServeOptions.md#baseuri)
- [development](https://github.com/oven-sh/bun-types/blob/master/api-docs/interfaces/bun_.ServeOptions.md#development)
- [error](https://github.com/oven-sh/bun-types/blob/master/api-docs/interfaces/bun_.ServeOptions.md#error)
- [hostname](https://github.com/oven-sh/bun-types/blob/master/api-docs/interfaces/bun_.ServeOptions.md#hostname)
- [maxRequestBodySize](https://github.com/oven-sh/bun-types/blob/master/api-docs/interfaces/bun_.ServeOptions.md#maxrequestbodysize)
- [port](https://github.com/oven-sh/bun-types/blob/master/api-docs/interfaces/bun_.ServeOptions.md#port)

### Methods

- [fetch](https://github.com/oven-sh/bun-types/blob/master/api-docs/interfaces/bun_.ServeOptions.md#fetch)

## Properties

### baseURI

• `Optional` **baseURI**: `string`

What URI should be used to make Request.url absolute?

By default, looks at [hostname](https://github.com/oven-sh/bun-types/blob/master/api-docs/interfaces/bun_.ServeOptions.md#hostname), [port](https://github.com/oven-sh/bun-types/blob/master/api-docs/interfaces/bun_.ServeOptions.md#port), and whether or not SSL is enabled to generate one

**`Example`**

```js
"http://my-app.com"
```

**`Example`**

```js
"https://wongmjane.com/"
```

This should be the public, absolute URL – include the protocol and [hostname](https://github.com/oven-sh/bun-types/blob/master/api-docs/interfaces/bun_.ServeOptions.md#hostname). If the port isn't 80 or 443, then include the [port](https://github.com/oven-sh/bun-types/blob/master/api-docs/interfaces/bun_.ServeOptions.md#port) too.

**`Example`**

```ts
"http://localhost:3000"
```

___

### development

• `Optional` **development**: `boolean`

Render contextual errors? This enables bun's error page

**`Default`**

process.env.NODE_ENV !== 'production'

___

### error

• `Optional` **error**: (`this`: [`Server`](https://github.com/oven-sh/bun-types/blob/master/api-docs/interfaces/bun_.Server.md), `request`: [`Errorlike`](https://github.com/oven-sh/bun-types/blob/master/api-docs/interfaces/bun_.Errorlike.md)) => `Response` \| `Promise`<`Response`\> \| `Promise`<`undefined`\>

#### Type declaration

▸ (`this`, `request`): `Response` \| `Promise`<`Response`\> \| `Promise`<`undefined`\>

##### Parameters

| Name | Type |
| :------ | :------ |
| `this` | [`Server`](https://github.com/oven-sh/bun-types/blob/master/api-docs/interfaces/bun_.Server.md) |
| `request` | [`Errorlike`](https://github.com/oven-sh/bun-types/blob/master/api-docs/interfaces/bun_.Errorlike.md) |

##### Returns

`Response` \| `Promise`<`Response`\> \| `Promise`<`undefined`\>

___

### hostname

• `Optional` **hostname**: `string`

What hostname should the server listen on?

**`Default`**

```js
"0.0.0.0" // listen on all interfaces
```

**`Example`**

```js
"127.0.0.1" // Only listen locally
```

**`Example`**

```js
"remix.run" // Only listen on remix.run
````

note: hostname should not include a {@link port}

___

### maxRequestBodySize

• `Optional` **maxRequestBodySize**: `number`

What is the maximum size of a request body? (in bytes)

**`Default`**

1024 * 1024 * 128 // 128MB

___

### port

• `Optional` **port**: `string` \| `number`

What port should the server listen on?

**`Default`**

process.env.PORT || "3000"

## Methods

### fetch

▸ **fetch**(`this`, `request`): `Response` \| `Promise`<`Response`\>

Handle HTTP requests

Respond to Request objects with a Response object.

#### Parameters

| Name | Type |
| :------ | :------ |
| `this` | [`Server`](https://github.com/oven-sh/bun-types/blob/master/api-docs/interfaces/bun_.Server.md) |
| `request` | `Request` |

#### Returns

`Response` \| `Promise`<`Response`\>

▸ **fetch**(`this`, `request`): `Response` \| `Promise`<`Response`\>

Handle HTTP requests

Respond to Request objects with a Response object.

#### Parameters

| Name | Type |
| :------ | :------ |
| `this` | [`Server`](https://github.com/oven-sh/bun-types/blob/master/api-docs/interfaces/bun_.Server.md) |
| `request` | `Request` |

#### Returns

`Response` \| `Promise`<`Response`\>