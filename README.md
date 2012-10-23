factcheck
=========

This is a mobile application written in HTML5/CSS3/Javascript. All code resides in the gh-pages branch.

Designed just prior to the Obama/Romney presidential debate Oct 22, 2012, the application worked fine leading up the the initial minutes of the debate, pulled in only a couple initial tweets from Politifact, then displayed black screens during for approx the next 50 minutes, then started functioning again.

During the time the twitter feeds all displayed black screens, I accessed the original Twitter feeds directly on the Twitter site, found that Politifact was not displaying any new Tweets during most of the time it was offline in this app, only gradually adding a couple tweets towards the end of the blackout. During the time the Twitter feed was offline, it displayed an HTTP 400 error, stating that the resource was non-existent. Note non-existent, not unavailable or no response. There is no problem when the Twitter feed issue was addressed soon before the end of the debate and currently.

Based on this circumstantial evidence the following assumptions and conjectures
- Twitter itself crashed for one of the feeds and was the primary cause of this appliation's own non-functionality.
- Although this application makes separate HTTP requests for each Twitter feed, the local browser engine may place all such JSON requests on a single thread so  that when one feed fails, all feeds fail. Otherwise, the HTML application functions unaffeccted, and other websites can also be accessed although subjectively slower than expected.

Special notes:
The button navigation in the Header Toolbar functions only with up to jQuery Mobile 1.1. Later versions of jQuery Mobile introduce the navbar button object which seems to debrecate the use of ordinary buttons.

Not too much time was spent investigating, but the navbar button object did not function with the Twitter code. Unknown why this might be an issue.

Google Translate as usual worked well and as expected.

Using the multi-page template which loads all pages into the DOM works well in this application. Although the intial load time is long, it also likely means that the Twitter feeds are all pre-loaded and update continuously in the background.