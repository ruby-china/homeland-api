# 通知 - Notifications

## 获取用户的通知列表

```markup
GET /api/v3/notifications
```

### Parameters

* offset (Integer) - default: 0
* limit (Integer) - default: 20, range: 1..150

### Response

Array<[NotificationSerializer](NotificationSerializer)>

## 批量将通知设成已读状态

将当前用户的一些通知设成已读状态

```markup
POST /api/v3/notifications/read
```

### Parameters

* ids (Array) - 需要设为已读的通知编号列表（只能是当前用户的） [required]

## 获取未读通知数量

获得未读通知数量

```markup
GET /api/v3/notifications/unread_count
```

## 删除某个通知

删除当前用户的某个通知

```markup
DELETE /api/v3/notifications/:id
```

## 清空通知

删除当前用户的所有通知

```markup
DELETE /api/v3/notifications/all
```



