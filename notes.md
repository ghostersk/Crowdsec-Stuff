## Whitelist by AS Number
[Redit post source](https://www.reddit.com/r/CrowdSec/comments/1l7a5x6/comment/mwv6z0t/)
```
#/etc/crowdsec/postoverflows/s01-whitelist/asn-whitelist.yaml
name: zz-whitelist-ASN
description: Whitelist some ASN
#debug: true
whitelist:
  reason: Whitelisted ASN
  expression:
    - evt.Overflow.Alert.GetScenario() == 'LePresidente/http-generic-403-bf' && Lower(evt.Overflow.Alert.Source.AsName) contains 'vodafone'
```
