## Nicholas Hare

Noticed on my first glance at code immediately there was an extra comma amongst the bidder parameters.

Per: `“Ads appear to rendering sometimes successfully and sometimes not.  The page seems to break more often for users who are sitting on it for a long period of time.”`

I observed the page and the initial load appears to render properly but then shortly after is overtaken by a single refresh being called that is overtaking the entirety of the window.

Initially I removed to refresh to see if that was indeed the cause and it appeared to work as a "quick" fix but I was under the assumption that refresh was intended so I delved deeper. After investigating the code, namely the refresh and associated functions/methods I noticed it was writing over the docuement. Upon changing it to write over the ad unit's iframe I saw bid requests were being doubled on the refresh and that if the creative was of a different size the creative would not render properly.

## Fix

Reworked the refreshAD code. Removing addadunits from the pbjs call in the refresh. This keeps it at the expected bid requests while also properly rendering any creative.

