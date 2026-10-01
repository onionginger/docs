## Server side

Main server start file import socket mongo and startJobs for removing inactive 
chatrooms 

## Socket
-attachsocket(httpserver) create server set to cors on client server, all socket utils
    - 

## Image uploading
-const imageUpload() use multer to load file to disk storage with upload date, limit 
size to 5 mb and throw error if file not approved type 
-const publicPath(path) create route to file 
-removeUpload(urlPath) remove file from disk storage

## General utilities
-channelSlug(value) convert name to slug case
-escapeRegex(s) replace with valid regex
-cleanName(value, max) check channel string in character limit and trim bad regex

## Audit utilities



## Role checking
-publicUser(user, full is false) public return user function
-isMember(group, userid) check userids against member array
-isGroupAdmin(group, user) check user role is user and admin



## Admin utilities
-addMember() check user birthdate against age limit and update group members
-removeMember() kicked user from chatrooms and send audit for group change
-enforeAgeLimit() 
-createChannel() add to group channels, send audit
-deleteChannel() delete messages, send audit 
-historyFor(channel, group, userid) store user channel message history 


## Super admin utilities
-findGroup(id) returns group in group collection by id
-findChannel(id) return channel (chatroom) using findOne util id
-loadMemberGroup(req, res, next) loads groups user joined
-requireGroupAdmin(req, res, next) 
-channelIdsOf(groupId) retrieve channels in a group
-asserGroupNameFree() check for free names by filtering through goups 
-createGroup(name, admin, actor) create group object containing name, key, members array, banned users array, user requested group, and date created
-deleteGroup(group, actor) delete all group chats and channels (chatrooms) and show realtime notif for group change (?)

## Channel utilies
-deleteInactiveChannel() deletes any channel that recieved no activity in the last channelInactiveDays number of days by searching the channels db collection that meet the cutoff date from the 
-startJobs() runs chatroom deletion in the background at every hour with setInterval

## Audit services

## Authenticator services
