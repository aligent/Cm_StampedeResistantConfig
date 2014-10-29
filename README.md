Stampede-Resistant Config Cache
======

This modified version of Mage_Core_Model_Config fixes or at least improves the tendancy of high-traffic sites to cause stampeding issues around the config cache. This issue exists with all backends and is most prevelant in stores that have large configurations, many store scopes, or particularly slow cache backends.

TODO