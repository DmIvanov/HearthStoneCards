# HearthStoneCards

It's a sample app which uses HearthStone card game API from mashape.com:
https://market.mashape.com/omgvamp/hearthstone  
http://hearthstoneapi.com  

The app is capable for retrieving cards from the API and show them in a simple collection view with an ability to filter cards. It also contains detail for each card.

### Main concepts of the project are:
	- modularity 
	- clear object's responsibilities 
	- clear APIs 
	- testability

### What's implemented:
- Main Interactor for general business logic and switching between different scenes (register/login, profile,...), now there is only one of them implemented. The object will be usefull in case of further development of the project.
- Network Layer (URLSession, remote API call, response parsing)
- Data Service (which suppose to be passed between different scenes and between modules inside the scene)
- Image Manager (with ability to cache loaded images) - the only singletone in the app... after AppDelegate of course =)
- View Controller Factory - just one common place to instantiating view controllers. Can be more usefull in future if going for the scheme with Interactor(business logic) + Presenter(presenting logic, screen switching).
- 3 screens (UI + models): Collection, Detail view, Filters
- Some Unit Tests

### TODO:
- Proper logic of cache invalidation (now it's technically correct but has not much sence)
- Persistency (favourites, filters)
- Dealing with duplicates (there seem to be the same cards in different card sets, which I mix together)
