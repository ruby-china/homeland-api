# 点赞 - Likes

点赞可以针对 **话题（topic）或回帖（reply)** 发起。

## 点赞

对话题/回帖点赞

```markup
POST /api/v3/likes
```

### Parameters

* obj_type (String) — 类型 `[topic, reply]` 
* obj_id (Integer) — 对应数据的编号

### Response

* count [Integer] 已赞的数量

## 取消赞

取消之前的赞

```markup
DELETE /api/v3/likes
```

### Parameters

* obj_type (String) — 类型 `[topic, reply]` 
* obj_id (Integer) — 对应数据的编号



