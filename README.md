# ![LOGO](logo.png) Poly **flow**ground Connector

## Description

A generated **flow**ground connector for the Poly API (version v1).

Generated from: https://api.apis.guru/v2/specs/googleapis.com/poly/v1/swagger.json<br/>
Generated at: 2019-05-23T12:13:33+03:00

## API Description

The Poly API provides read access to assets hosted on <a href="https://poly.google.com">poly.google.com</a> to all, and upload access to <a href="https://poly.google.com">poly.google.com</a> for whitelisted accounts.


## Authorization

This API does not require authorization.

## Actions

### Lists all public, remixable assets. These are assets with an access level of<br/>
> PUBLIC and published under the<br/>
> CC-By license.

*Tags:* `assets`

#### Input Parameters
* `category` - _optional_ - Filter assets based on the specified category. Supported values are:
`animals`, `architecture`, `art`, `food`, `nature`, `objects`, `people`, `scenes`,
`technology`, and `transport`.
* `curated` - _optional_ - Return only assets that have been curated by the Poly team.
* `format` - _optional_ - Return only assets with the matching format. Acceptable values are:
`BLOCKS`, `FBX`, `GLTF`, `GLTF2`, `OBJ`, `TILT`.
* `keywords` - _optional_ - One or more search terms to be matched against all text that Poly has
indexed for assets, which includes display_name,
description, and tags. Multiple keywords should be
separated by spaces.
* `maxComplexity` - _optional_ - Returns assets that are of the specified complexity or less. Defaults to
COMPLEX. For example, a request for
MEDIUM assets also includes
SIMPLE assets.
    Possible values: COMPLEXITY_UNSPECIFIED, COMPLEX, MEDIUM, SIMPLE.
* `orderBy` - _optional_ - Specifies an ordering for assets. Acceptable values are:
`BEST`, `NEWEST`, `OLDEST`. Defaults to `BEST`, which ranks assets
based on a combination of popularity and other features.
* `pageSize` - _optional_ - The maximum number of assets to be returned. This value must be between `1`
and `100`. Defaults to `20`.
* `pageToken` - _optional_ - Specifies a continuation token from a previous search whose results were
split into multiple pages. To get the next page, submit the same request
specifying the value from next_page_token.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Returns detailed information about an asset given its name.<br/>
> PRIVATE assets are returned only if<br/>
>  the currently authenticated user (via OAuth token) is the author of the asset.

*Tags:* `assets`

#### Input Parameters
* `name` - _required_ - Required. An asset's name in the form `assets/{ASSET_ID}`.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Lists assets authored by the given user. Only the value 'me', representing<br/>
> the currently-authenticated user, is supported. May include assets with an<br/>
> access level of PRIVATE or<br/>
> UNLISTED and assets which are<br/>
> All Rights Reserved for the<br/>
> currently-authenticated user.

*Tags:* `users`

#### Input Parameters
* `format` - _optional_ - Return only assets with the matching format. Acceptable values are:
`BLOCKS`, `FBX`, `GLTF`, `GLTF2`, `OBJ`, and `TILT`.
* `name` - _required_ - A valid user id. Currently, only the special value 'me', representing the
currently-authenticated user is supported. To use 'me', you must pass
an OAuth token with the request.
* `orderBy` - _optional_ - Specifies an ordering for assets. Acceptable values are:
`BEST`, `NEWEST`, `OLDEST`. Defaults to `BEST`, which ranks assets
based on a combination of popularity and other features.
* `pageSize` - _optional_ - The maximum number of assets to be returned. This value must be between `1`
and `100`. Defaults to `20`.
* `pageToken` - _optional_ - Specifies a continuation token from a previous search whose results were
split into multiple pages. To get the next page, submit the same request
specifying the value from
next_page_token.
* `visibility` - _optional_ - The visibility of the assets to be returned.
Defaults to VISIBILITY_UNSPECIFIED which returns all assets.
    Possible values: VISIBILITY_UNSPECIFIED, PUBLISHED, PRIVATE.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Lists assets that the user has liked. Only the value 'me', representing<br/>
> the currently-authenticated user, is supported. May include assets with an<br/>
> access level of UNLISTED.

*Tags:* `users`

#### Input Parameters
* `format` - _optional_ - Return only assets with the matching format. Acceptable values are:
`BLOCKS`, `FBX`, `GLTF`, `GLTF2`, `OBJ`, `TILT`.
* `name` - _required_ - A valid user id. Currently, only the special value 'me', representing the
currently-authenticated user is supported. To use 'me', you must pass
an OAuth token with the request.
* `orderBy` - _optional_ - Specifies an ordering for assets. Acceptable values are:
`BEST`, `NEWEST`, `OLDEST`, 'LIKED_TIME'. Defaults to `LIKED_TIME`, which
ranks assets based on how recently they were liked.
* `pageSize` - _optional_ - The maximum number of assets to be returned. This value must be between `1`
and `100`. Defaults to `20`.
* `pageToken` - _optional_ - Specifies a continuation token from a previous search whose results were
split into multiple pages. To get the next page, submit the same request
specifying the value from
next_page_token.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

## License

**flow**ground :- Telekom iPaaS / googleapis-com-poly-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
