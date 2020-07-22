# 图片附件 - Photos

## 上传附件

上传图片,请使用 Multipart 的方式提交图片文件.

```markup
POST /api/v3/photos
```

### Parameters

* file - 文件信息, [required]

### Response

```json
{
  image_url: '图片 URL',
}
```



