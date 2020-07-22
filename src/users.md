# 账号 - Users

## 获取热门用户

```markup
GET /api/v3/users
```

### Parameters

* limit (Integer)  - default: 20，range: 1..100

### Response

Array<[UserSerializer](/ruby-china/api/UserSerializer)>

## 获取某个用户的详细信息

获取 `:id` 用户的详细信息

```markup
GET /api/v3/users/:id
```

### Response

[UserDetailSerializer](/ruby-china/api/UserDetailSerializer)

## 获取当前用户的完整信息

用于个人设置修改资料

```markup
GET /api/v3/users/me
```

### Response

[UserDetailSerializer](/ruby-china/api/UserDetailSerializer)

## 用户回帖列表

获取某个用户的回帖列表

```markup
GET /api/v3/users/:id/replies
```

## 用户的话题列表

获取某个用户发布的话题列表

```markup
GET /api/v3/users/:id/topics
```

### Parameters

* order (String) - 排序方式, default: 'recent', range: %w(recent likes replies)
* offset (Integer) - default: 0
* limit (Integer) - default: 20, range: 1..150

### Response

Array<[TopicSerializer](/ruby-china/api/TopicSerializer)>

## 屏蔽用户

当前用户屏蔽 `:id` 的用户

```markup
POST /api/v3/users/:id/block
```

## 取消屏蔽用户

当前用户取消屏蔽 `:id` 的用户

```markup
POST /api/v3/users/:id/unblock
```

## 获取当前用户的屏蔽列表

获取当前用户的已屏蔽的人（只能获取自己的）

```markup
GET /api/v3/users/:id/blocked
```

### Parameters

* offset (Integer) - default: 0
* limit (Integer) - default: 20, range: 1..150

### Response

Array<[UserSerializer](/ruby-china/api/UserSerializer)>

## 关注用户

当前用户关注 `:id` 的用户

```markup
POST /api/v3/users/:id/follow
```

## 取消关注

当前用户取消对 `:id` 用户的关注

```markup
POST /api/v3/users/:id/unfollow
```

## 获取用户的关注列表

获取 `:id` 的用户的关注列表

```markup
GET /api/v3/users/:id/following
```

### Parameters:

* offset (Integer) - default: 0
* limit (Integer) - default: 20, range: 1..150

### Response

Array<[UserSerializer](/ruby-china/api/UserSerializer)>

## 获取用户的关注者列表

获取关注 `:id` 用户的人的列表

```markup
GET /api/v3/users/:id/followers
```

### Parameters:

* offset (Integer) - default: 0
* limit (Integer) - default: 20, range: 1..150

### Response

Array<[UserSerializer](/ruby-china/api/UserSerializer)>

## 获取某个用户的收藏列表

获取 `:id` 用户收藏的话题列表

```markup
GET /api/v3/users/:id/favorites
```

### Parameters:

* offset (Integer) - default: 0
* limit (Integer) - default: 20, range: 1..150

### Response

Array<[TopicSerializer](/ruby-china/api/TopicSerializer)>

