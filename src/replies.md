# 回帖 - Replies

## 获取回帖的详细内容

获取回帖的详细内容（一般用于编辑回帖的时候）

```markup
GET /api/v3/replies/:id
```

### Response

[ReplyDetailSerializer](ReplyDetailSerializer)

## 修改回帖

```markup
POST /api/v3/replies/:id
```

### Parameters

* body (String) - 回帖内容 [required]

### Response

[ReplyDetailSerializer](ReplyDetailSerializer) - 更新过后的数据

## 删除回帖

```markup
DELETE /api/v3/replies/:id
```



