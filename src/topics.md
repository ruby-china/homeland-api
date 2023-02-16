# 话题 - Topics

## 获取话题列表

获取话题列表，类似 Ruby China [话题列表](https://ruby-china.org/topics)的内容，支持多种排序方式。

```markup
GET /api/v3/topics
```

### Parameters:

* type (String) - 排序类型，default: `last_actived`
    * 可选值：`last_actived, recent, no_reply, popular, excellent`
* node_id (Integer) - 节点编号，如果有给，就会只去节点下的话题
* offset (Integer) - default: 0
* limit (Integer) - default: 20, range: 1..150

### Response

Array<[TopicSerializer](TopicSerializer.md)>

## 话题详情

获取话题详情（不含回帖）

```markup
GET /api/v3/topics/:id
```

### Response

[TopicDetailSerializer](TopicDetailSerializer.md)

## 创建新话题

创建一篇新的话题

```markup
POST /api/v3/topics
```

### Parameters:

* title (String) — 标题，[required]
* node_id (Integer) — 节点编号，[required]
* body (Markdown) — 格式的正文，[required]

### Response

[TopicDetailSerializer](TopicDetailSerializer.md)

## 修改话题

修改话题内容

```markup
PUT /api/v3/topics/:id
```

### Parameters

* title (String) — 标题，[required]
* node_id (Integer) — 节点编号，[required]
* body (Markdown) — 格式的正文，[required]

### Response

[TopicDetailSerializer](TopicDetailSerializer.md)

## 删除话题

删除一篇话题

```markup
DELETE /api/v3/topics/:id
```

## 创建回帖

创建对 `:id` 话题的回帖

```markup
POST /api/v3/topics/:id/replies
```

### Parameters

* body (String) - 回帖正文

### Response

[ReplySerializer](ReplySerializer.md)

## 话题的回帖列表

获取话题的回帖列表

```markup
GET /api/v3/topics/:id/replies
```

### Parameters

* offset (Integer) - default: 0
* limit (Integer) - default: 20, range: 1..150

### Response

Array<[ReplySerializer](ReplySerializer.md)>

## 关注话题

```markup
POST /api/v3/topics/:id/follow
```

## 取消关注话题

```markup
POST /api/v3/topics/:id/unfollow
```

## 收藏话题

```markup
POST /api/v3/topics/:id/favorite
```

## 取消收藏话题

```markup
POST /api/v3/topics/:id/unfavorite
```

## 话题动作接口

对 `:id` 这篇话题发起动作（屏蔽、加精华、结束讨论...）注意类型有不同的权限，详见 `GET /api/v3/topics/:id` 返回的 `abilities`

```
POST /api/v3/topics/:id/action?type=:type
```

### Parameters:

* type (String) — 动作类型，ban - 屏蔽话题，excellent - 加精华，unexcellent - 去掉精华，close - 关闭回复，open - 开启回复



