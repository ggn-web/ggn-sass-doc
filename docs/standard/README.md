# 前端规范

## 命名

### 1.文件夹命名

> 采用小写方式，当有以复数名字时，以中划线—分隔

::: tip 例子

- head-search / page-loading / authorized / notice-icon
  :::

### 2.文件命名

> 全部采用小写方式， 以中划线-分隔，\*.vue 文件除外，vue 文件采用驼峰首字母大写方式

::: tip 例子

- render-dom.js / signup.css / index.html / company-logo.png
- List.vue / UserList / ProjectManageList
  :::

### 3.注意点

::: warning 命名（这个适用于所有命名，文件，文件夹，变量，函数等）

1. 名字的单词不要超过三级，ProjectManageList 这种已经是极限
2. 命名严禁使用拼音与英文混合的方式，更不允许直接使用中文的方式
3. 杜绝完全不规范的缩写，避免望文不知义
   :::
   ::: danger 错误示范

- vue 文件：MyProjectManageList.vue
- 文件夹/文件名：my-project-add-edit
- AbstractClass“缩写”命名成 AbsClass；condition“缩写”命名成 condi
  :::

## Css/Sass 规范

::: tip 注意点

1. 类名使用小写字母，以中划线分隔
2. 称总是使用可以反应元素目的和用途的名称，或其他通用的名称，代替表象和晦涩难懂的名称

```css
/* 不推荐 */
.fw-800 {
  font-weight: 800;
}
.red {
  color: red;
}
/* 推荐 */
.heavy {
  font-weight: 800;
}
.important {
  color: red;
}
```

3. 名称中划线-连接最多三级，不可超过三级
4. css 选择器中避免使用标签名，实在要用要配合直接子选择器

```css
.content > .title {
  font-size: 2rem;
}
```

5. scss 中的变量、函数、混合、placeholder 采用驼峰式命名
6. 尽量使用缩写属性

```css
/* 不推荐 */
padding-bottom: 2em;
padding-left: 1em;
padding-right: 1em;
padding-top: 0;
/* 推荐 */
padding: 0 1em 2em;
```

7. 每个选择器及属性独占一行

```css
.primary-button {
  width: 100px;
  height: 50px;
  color: #fff;
  background: #00a0e9;
}
```

8. 省略 0 后面的单位

```css
.title {
  padding-bottom: 0;
  margin: 0;
}
```

9. 避免使用ID选择器及全局标签选择器防止污染全局样式,尽可能使用class
10.  <font color=red>避免嵌套层级过多，最多三层嵌套</font>

:::

## Javascript规范

::: tip 注意点
1. 方法名、参数名、成员变量、局部变量都统一使用小写驼峰命名
2. method 方法命名必须是 动词 或者 动词+名词 形式
3. 增删查改，详情 ———命名可以参照下面的5 个单词
``` js
add / update / delete / detail / get
```
4. 尽量使用ES6,ES7语法，不要用var这些
5. 条件判断和循环最多三层
6. console.log，debugger等调试使用的代码用完一定要删除
:::

## Vue项目规范