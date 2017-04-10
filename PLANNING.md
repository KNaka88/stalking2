MVP
  * As a user, I can register and signin the page
  * As a user, I am navigated to my own account page (dynamic routing)
  * As a user, I can check where I am located at google map
  * As a user, I can see others' location
  * As a user, if I clicked the pin on map, I can check others name, last updated time
  * As a user, I can log out from the page


Additional
  * As a user, I can click others pin and send messages
  * As a user, I can recieve message from others
  * As a user, I can see all messages I sent
  * As a user, I can see all messages I received


More Additional
  * As a user, I can edit or delete message what I sent
  * As a user, I can see only messages I sent to specific person
  * As a user, I can see only messages I received from specific person


Advanced
  * As a user, I can send friend request
  * As a user, I can confirm or decline the friend request  
  * User can send message only they become as friends



Component
* app page (template)
  -- app.component.ts
    -- constructor: check user is logged in or not and navigate to

* login-page (google signin, and normal login page)
  -- login-page.component.ts
    -- login(): -> user-service login() -> firebase
    -- loginGoogle(): -> user-service loginGoogle() -> firebase

  -- login-page.component.html
    -- signin form (normal, google account)
    -- a routerlink: create new account -> registration-page.html



* registration-page (new member page)
  -- registration-page.component.ts


    --

  -- registration-page.component.html





Service ( same functionallity as af.ts)
* user service

    login & logout
      -- login()
      -- loginWithGoogle()
      -- logout
    



    -- getUserName
    -- getUserEmail
    -- getUserId








Model
* user class
    -- uid (firebase generated)
    -- name: string
    -- email: string
    -- lat: number (latest location)
    -- lng: number (latest location)
    -- sentMessage
        -- uid (firebase generated?)
        -- to whom: string (uid of person who want to send message to)
        -- lat: number
        -- lng: number
        -- message: string
        -- date: string
    -- receivedMessage
        -- uid (firebase generated?)
        -- from whom: string (uid of person who sent message from)
        -- lat: number
        -- lng: number
        -- message: string
        -- timestamp: string
