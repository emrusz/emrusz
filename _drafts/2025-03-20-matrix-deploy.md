---
title: "Migrating to a new Matrix Homeserver"
categories:
  - communication
tags:
  - element
  - matrix
---

## Account Migration

Element offers an experimental service to migrate to your new account, but it requires handing over the credentials to both your old and new accounts.

> [!NOTE]
> Test

### Key Backup

To maintain access to older messages you must first export your backup encryption keys from Element.

### Direct Messages

Direct messages can be transferred to your new account with a few simple steps. It's possible to maintain the history because Matrix allows users to freely convert chats between direct messages and rooms.

1. Invite the new account. The direct message will be automatically converted to a room.

```
/invite @new:new-server.tld
```

2. Elevate the new account to level 100 (admin). Matrix treats all users in a direct message as administrators by default.

```
  /op @new 100
```

3. Verify you can view your message history from the new account.
4. Kick the old account from the room.

```
/kick @old`
```

5. Convert the room back to a direct message.

```
  /converttodm
```
