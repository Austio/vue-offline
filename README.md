# Vue Offline

Initial planning concepts for Vue Offline using Vuex.

1 Meta Data attached to action like thing that allow for
 - Action
 - What do do on success
 - What to do on failure
 - Optimistic
 - Rollback
 - Retries
 - Unique ID
 - Concurrent or Sequential (After another condition)
 
2. Some worker that will go through the queue (maybe via a setTimeout or something that will not block) 
 
3. Optionally Persist Store between Reloads (plugin to listen to state changes) 


## Usage Scenarios

### Normal Offline Actions

### Pre Caching Queries

Consider based on some deterministic action we know there is some reasonable likelihood of another action.  It may make sense to precache that data so taht it is available when needed.  

We could queue up several requests to load up an index page and the next likely place that will be requested.  Those requests could be returned as part of an SSR or any other type of request and pushed to our store and worked.

