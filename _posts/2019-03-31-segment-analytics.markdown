Using Segment and Google Analytics to easily track custom events

"Truth is ever to be found in simplicity, and not in the multiplicity and confusion of things"

This quote from Newton has recently become my motto in life. Along with the atomic approach to 
problem solving, these two ideas together become a very powerful concept to remind yourself of 
whenever a challenge comes up.

Not that integrating simple analytics into a project is anything very complicated to accomplish, 
however it's not hard to find some API documentations out there that instead of clarifying stuff,
leaves you even more confused than when you started reading them (btw, amazing documentation 
was one of the key factors to Stripe's success). 

On that matter, Segment stuck with Newton: simple, straight to the point. Let's suppose you have
a search bar and you need to track searched words. Check this out:

analytics.track()

Wow! Really? Yup.

However, since Segment is pretty much a hub for you send your data and then choose to which other
destination you want to send it, and we use Google Analytics we needed to get 



