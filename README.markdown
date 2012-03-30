PullToRefresh-Sencha-Touch-2.0-w-loading-tweaks
===============================================

A tweaked version of the PullRefresh Plugin that ships with Sencha 2.0.

This is a revision we created for use in one of our apps. When looking at how pull-to-refresh works it seemed odd to us that the loading box snapped out of view before the content was actually updated. This keeps the loader in view until the data is updated. Providing for a better user experience and helping the user see something is still happening. 


Implementing this Version
---------------------------
Simply replace the PullRefresh.js file found in sdk/plugins/ with the version from the repo. 


Reverting to Sencha Default
---------------------------
Replace the file with the original from the Sencha 2.0 SDK.

Additionally we left Sencha's original method on line 307. To see the original functionality uncomment the function found on line 308. Then comment 301-305 & 221-223.