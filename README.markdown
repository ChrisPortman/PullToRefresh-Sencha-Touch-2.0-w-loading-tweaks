NOTICE: STILL BUG TESTING THIS BRANCH

I realized that this plugin is not handling deletion of records. After some digging I found a <a href="http://www.sencha.com/forum/showthread.php?196465-pullrefresh-plugin-does-not-handle-deletion-of-records">forum post<a/> where FrankK had already begun to do some work at adding a deletion method. Simple adding his code works for deleting records but it introduced a new bug. Because the records are being deleted the height of the viewport is changing and the PullRefresh window is no longer out of view. FrankK's code works with the sencha default plugin because the scroller is being hidden before the records change. However that is not my goal. I want it to stay in view until the records are updated.

That being said I'm still working to figure out how to achieve this. Hence this branch.


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