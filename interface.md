# 前端接口文档

## 文章接口

### 文章列表(get /articles)

#### 接口请求参数

```json
当前页数：page
每页数据条数：limit
搜素关键字：search
分类或标签Id：mid
```

例如：`/articles?page=1&limit=10&search=xxx&mid=1`

#### 接口结果返回

```json
// 成功时返回
{
	"success": true,
	"data": {
		"list": [
			{
				"aid": 1,
				"title": "article name",
				"slug": "article slug",
				"updated_at": "1469636493",
				"text": "blog text",
				"userName": "cookfront",
				"commentsNum": 5,
			}
		],
		"pageSize": 10,
		"totalCount": 100
	}
}
```

### 新增或更新文章(post /articles)

#### 接口请求参数

```json
文章标题：title
文章内容：text
是否允许评论：allowComment
公开度：status
分类：category
标签：tags
```

#### 接口结果返回

```json
{
	"success": true,
	"cid": 1
}
```

### 根据ID获取文章信息(get /articles/:id)

#### 接口结果返回

```json
{
	"success": true,
	"data": {
		"cid": 1,
		"title": "article name",
		"slug": "article slug",
		"updated_at": "1469636493",
		"text": "blog text",
		"userName": "cookfront",
		"commentsNum": 5,
	}
}
```

### 根据ID删除文章(delete /articles/:id)

#### 接口结果返回

```json
{
	"success": true,
	"id": 1
}
```

### 根据用户ID获取文章列表(get /articles/author/:userId)

#### 接口请求参数

```json
当前页数：page
每页数据条数：limit
搜素关键字：search
分类或标签Id：mid
```

#### 接口结果返回

```json
{
	"success": true,
	"msg": "",
	"data": {
		"list": [
			{
				"aid": 1,
				"title": "article name",
				"slug": "article slug",
				"updated_at": "1469636493",
				"text": "blog text",
				"userName": "cookfront",
				"commentsNum": 5,
			}
		],
		"pageSize": 10,
		"totalCount": 100
	}
}
```

## 分类接口

### 获取分类列表(get /categories)

### 新增和更新分类(pot /categories)

### 根据ID获取分类信息(get /categories/:id)

### 根据ID删除分类(delete /categories/:id)

## 标签接口

### 获取标签列表(get /tags)

### 新增和更新标签(post /tags)

### 根据ID获取标签信息(get /tags/:id)

### 根据ID删除标签(delete /tags/:id)

## 评论接口

### 获取评论列表(get /comments)

### 根据博客ID获取评论列表(get /comments?aid=12)

### 新增评论(post /comments)

### 更新评论(put /comments/:id)

### 根据ID删除评论(delete /comments/:id)

### 根据多个ID批量删除评论

### 根据多个ID审核评论

### 根据ID审核评论

### 回复评论

## 用户接口

### 用户登录

### 获取用户列表(get /users)

### 新增用户(post /users)

### 更新用户(put /users/:id)

### 根据ID删除用户(delte /users/:id)
