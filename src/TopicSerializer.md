# TopicSerializer

话题信息，一般在列表返回的时候出现。

## attributes

* **id** [Integer] 话题编号
* **title** [String] 标题
* **node_name** [String] 节点名称
* **node_id** [Integer] 节点 ID
* **excellent** [Boolean] 是否精华
* **deleted** [Boolean] 是否已删除
* **replies_count** [Integer] 回帖数量
* **likes_count** [Integer] 赞数量
* **last_reply_user_id** [Integer] 最后回复人用户编号
* **last_reply_user_login** [String] 最后回复者 login
* **user** [UserSerializer](UserSerializer) 最后回复者用户对象
* **replied_at** [DateTime] 最后回帖时间
* **created_at** [DateTime] 创建时间
* **updated_at** [DateTime] 更新时间



