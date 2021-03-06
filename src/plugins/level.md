# Level plugin

The level plugin provides xp to your users as they speak in chat!

## Commands

| Name                                     | Description                                                                                                                                                                 | Default Level | Usage                                                               |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|---------------------------------------------------------------------|
| `!xp [user]`                             | Checks your own, or another user's XP and level                                                                                                                             | Default       | `!xp` OR `!xp @ZeroMomentum`                                        |
| `!xp block {user}`                       | Blocks a user from gaining XP                                                                                                                                               | Moderator     | `!xp block 435206857276260353` OR `!xp block @ZeroMomentum`         |
| `!xp unblock {user}`                     | Removes a user's XP block                                                                                                                                                   | Moderator     | `!xp unblock 435206857276260353` OR `!xp unblock @ZeroMomentum`     |
| `!xp give {user} {amount}`               | Gives a user {amount} amount of XP                                                                                                                                          | Admin         | `!xp give @ZeroMomentum 1234` OR `!xp give 435206857276260353 1234` |
| `!xp take {user} {amount}`               | Take {amount} XP from the user                                                                                                                                              | Admin         | `!xp take @ZeroMomentum 1234` OR `!xp take 435206857276260353 1234` |
| `!xp reset {user}`                       | Completely removes a user's XP and sets it to 0                                                                                                                             | Admin         | `!xp reset @ZeroMomentum` OR `!xp reset 435206857276260353`         |
| `!xp top/leaderboard [places] [offset]`  | Shows the top 10 users of the leaderboard, using [places] instead of 10 if specified. If [offset] is specified, the leaderboard starts from [offset] instead of 1st place.  | Default       | `!xp top`, `!xp top 25 10` (shows the top 10-25)                    |

## Configuration Options
| Option  | Description                                                               | Type | Default |
|---------|---------------------------------------------------------------------------|------|---------|
| message | Whether to send the level up message in Direct Messages                   | bool | false   |
| chat    | Whether to send the level up message in the channel they leveled up in    | bool | true    |
| roles   | Mapping of levels: role_ids to give users when they reach a certain level | dict | empty   |

## Configuration Example
```yaml
level:
  message: false
  chat: true
  roles:
    5: 786653299268780083
    10: 791942837461581824
```
