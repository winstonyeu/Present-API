# python-present
A Python 3 client for Present API


**Authenticatication**
--------------------------
**Authenticating a user**

Logging in to retrieve and sets the access token

 ```python
from PresentAPI import PresentAPI

api = PresentAPI()
api.loginUser("email", "password")
 ```

**Data Retrieval**
--------------------------
Account:
```
api.loginUser("email", "password")
api.logoutUser()
api.registerUser("name", "email", "password")
```

User:
```
api.me()
api.getUser(email)
api.updateName(name)
api.updateAbout(about)
api.changeDisplayPicture(dp)
```

Relationship:
```
api.getfollower()
api.getfollowing()
api.checkFollowingStatus()
api.followUser(user_id)
api.unfollowUser(user_id)
```


**Error Handling**
--------------------------
 ```python
 from PresentAPI import PresentAPIError

 try:
    # code
 except PresentAPIError as e:
    if (e.status_code == 429):
        print ("Rate limit exceeded.")
 ```