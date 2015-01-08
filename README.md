Stampede-Resistant Config Cache
======

This modified version of Mage_Core_Model_Config fixes or at least improves the tendancy of high-traffic sites to cause stampeding issues around the config cache. This issue exists with all backends and is most prevelant in stores that have large configurations, many store scopes, or particularly slow cache backends.

The changes are as follows:

* If the cache lock flag is present, sleep for half a second and check again for up to 5 seconds rather than immediately considering the request a miss.
* Start the cache lock as soon as save starts rather than after separating and serializing the sub-sections.
* Do not clear the config tag when saving the cache.

About This Repository
======

This repository contains a Composer installable version of Colin Mollenhour's work (https://gist.github.com/colinmollenhour/7a91c4a92ccfd2adaeb6).  Colin deserves all of the credit for the idea and it's implementation, we just did the composer.json!
