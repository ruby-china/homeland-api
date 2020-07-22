# ReplyDetailSerializer

包含原始正文 Markdown 信息的回帖

## attributes

* **id** [Integer] 编号
* **body_html** [String] 以转换成 HTML 的正文
* **topic_id** [Integer] 话题编号
* **deleted** [Boolean] 是否已删除
* **likes_count** [Integer] 赞数量
* **user** [UserSerializer](UserSerializer.md) 最后回复者用户对象
* **created_at** [DateTime] 创建时间
* **updated_at** [DateTime] 更新时间
* **topic_title** [String] 话题标题
* **body** [String] 回帖正文，原始 Markdown



