# Componentized-name-rules(neo组件化命名规范)

<br/>

这是一套可以应用在任何界面的简单的组件化命名解决方案（即使是纯html、css环境依然适用），特别适合包装一些不需要组件化的小型vue组件。

**优点：样式定位准确，逻辑清晰，规则简单，可读性高，一目了然，无冲突，可复用。只需要一两种选择器就可以选择任何想要选择的元素。**

<br/>
<br/>

## 统一原则：

(前缀) (_全局||不相关) (PG||UI) (-分割) (驼峰名称)

```
// vue加入页面的分层
_PG-name
  name_PG-子页面
  
    // 页内组件
    p_UI-xxx  定义组件（加p（代表page）以区分全局组件）
      ├ui-x-xxx    定义子元素
```

```
// 全局组件
_UI-aaa
├ui-a-aaa
├ui-a-bbb
└─ui-a-b-ccc

// 页内组件
p_UI-bbb
├ui-b-aaa
├ui-b-bbb
└─ui-b-b-ccc
```

```
// css全局样式（无前缀）应用：class=“p_UI-xxx _pa _cl-aaa”
_pa
_pr
```

```
// 选择器
(.name_PG-index ._UI-aaa .ui-a-xxx)
```

**本规范不限定任何使用方式，你可以自由调整。（规则是死的，人是活的。）**

<br/>
<br/>

## 截图 组件 | 组件-子组件 | 组件-所有子元素

<br/>

![image](README/1.png)

<br/>
<br/>

![image](README/2.png)

### 实例代码：

[vha-appDemo (Github)](https://github.com/neoStudioGroup/vha-appDemo)