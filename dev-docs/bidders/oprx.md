---
layout: bidder
title: oprx
description: Prebid OPRx Bidder Adaptor
pbjs: true
biddercode: oprx
media_types: banner, native
tcfeu_supported: false
usp_supported: true
coppa_supported: true
gpp_sids: usstate_all, usnat
schain_supported: false
safeframes_ok: false
ortb_blocking_supported: false
dsa_supported: false
deals_supported: true
floors_supported: true
sidebarType: 1
---
### Registration

For assistance or setup instructions, please contact us at <adsupport@optimizerx.com>.

### Banner Params

{: .table .table-bordered .table-striped }
| Name           | Scope     | Description               | Example              |  Type     |
|----------------|-----------|-------------------------- |----------------      |----------|
| `key`          | required  | The publisher account Key | `'adskj34sdfadfasd'` | `string` |
| `placement_id` | required  | Placement Id              | `110044`             | `number` |
| `height`       | optional  | Height of the creative    | `250`                | `number` |
| `width`        | optional  | Width of the creative     | `300`                | `number` |
| `bid_floor`    | optional  | Bid Floor Price           | `0.5`                | `decimal`|
| `npi`          | optional  | NPI                       | `'1234567890'`       | `string` |
| `ndc`          | optional  | NDC                       | `'1234-567-89'`      | `string` |

### AdUnit Format for Banner

```javascript
var adUnits = [
            {
                code: 'oprx-banner-ad',
                mediaTypes: {
                    banner: {
                        sizes: [[728, 90]]
                    }
                },
                bids: [{
                    bidder: 'oprx',
                    params: {
                        key
                        placement_id: 11223344,
                        height: 90,
                        width: 728,
                        bid_floor: 0.5,
                        npi: '1234567890',
                        ndc: '1234-567-89'
                    }
                }]
            }
        ];
```