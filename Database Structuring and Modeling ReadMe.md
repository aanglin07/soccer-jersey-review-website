# Jersey Review Website Database

## Mission Statement

The purpose of the Jersey Review Website database is to collect/gather soccer teams jersey information for soccer fans, 
so they have a centralized application where they can review, rate and access links to purchase these jerseys.

Mission Objective
*	Provide a list/collection of jerseys for different soccer teams.
*	Store user reviews and ratings for jerseys on the application
*	Store application user information.
*	Provide affiliate links to users to make purchases externally.

## Entity Relationship Model 

I am building a database to collect/store soccer teams jersey information. The requirements analysis identified that I would need the following entities:
*	User
*	Soccer Team
*	Soccer League
*	Jersey
*	Jersey Review
*	Jersey Rating
*	Wish Item
*	Login Information
*	Permissions





The relationships between these entities have been identified as follows:

*	A User can add one or more Jerseys to the collection; A Jersey can be added by one and only one User.
*	A User can add one or more Soccer Team; A Soccer Team can be added by one and only one User.
*	A User can add one or more Soccer League; A Soccer League can be added by one and only one User.
*	A User can add one or more Players; A Player can be added by one and only one User.
*	A User can have one or more Wish Items; A Wish Item can be for one or more Users.
*	A Soccer Team can have one or more Soccer League; A Soccer League can have one or more Soccer Team.
*	A Soccer Team can have one or more Jerseys; A Jersey can be associated with one and only one Soccer Team.
*	A Jersey can have one or more Jersey Reviews; A Jersey Review can be for one and only one Jersey.
*	A Jersey can be for one or more Wish Items; A Wish Item can have one and only one Jersey.
*	A Jersey can have one and only one Jersey Rating; A Jersey Rating can be for one and only one Jerseys.
*	A User can give one or more Jersey Reviews; A Jersey Review can have one or more ratings by Users.
*	A User can give one or more Jersey Rating; A Jersey Rating can have one or more rating by Users.
*	A User can have one and only one Login Information; Login Information can be for one and only one User.
*	A User can have one and only one Login Information; Login Information can be for one and only one User.
*	A User can have one or more Permissions; A Permission can be assigned to one or more Users.

## Entity Relationship Diagram

![Entity Relationship Diagram](https://user-images.githubusercontent.com/105037865/233810654-5ded0e5c-0464-4ece-8fcb-4a2dd2a2ed92.jpg)

 
## Relational Model

*	User (<ins>user_id</ins>, first_name, last_name, email, is_admin(fk) created_at, updated_at)
*	Soccer_Team (<ins>team_id</ins>, user_id(fk), team_name, created_at, updated_at)
*	Soccer_League (<ins>league_id</ins>, user_id(fk) league_name, created_at, updated_at)
*	Jersey (<ins>jersey_id</ins>, user_id(fk), team_id(fk), image, jersey_description, year, player_name, purchase_link, created_at, updated_at)
*	Jersey_Review (<ins>user_id(fk), jersey_id(fk)</ins>, review_comment, created_at, updated_at)
*	Jersey_Rating (<ins>user_id(fk), jersey_id(fk)</ins>, rating_number, created_at, updated_at)
*	Wish_Item (<ins>wish_item_id</ins>, user_id(fk), jersey_id(fk), created_at, updated_at)
*	Login_Info (<ins>login_id</ins>, user_id(fk), username, password, created_at, updated_at)
*	Permissions (<ins>permission_id</ins>, description, created_at, updated_at)
*	League_Team (<ins>league_id(fk), team_id(fk)</ins> , created_at, updated_at)
*	User_Permissions (<ins>user_id(fk), permission_id(fk)</ins> , created_at, updated_at)
*	User_Wish (<ins>wish_item_id(fk), user_id(fk)</ins> , created_at, updated_at)



