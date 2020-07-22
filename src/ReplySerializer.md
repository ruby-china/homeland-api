# ReplySerializer

回帖信息

## attributes

* **id** [Integer] 编号
* **body_html** [String] 以转换成 HTML 的正文
* **topic_id** [Integer] 话题编号
* **deleted** [Boolean] 是否已删除
* **likes_count** [Integer] 赞数量
* **user** [UserSerializer](UserSerializer) 最后回复者用户对象
* **created_at** [DateTime] 创建时间
* **updated_at** [DateTime] 更新时间



