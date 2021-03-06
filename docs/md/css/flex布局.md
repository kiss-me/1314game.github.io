# Flex 布局 （又称弹性布局）

## 容器

- 任何设置 `display: flex` 或者 `display: inline-flex` 属性的盒子都称为容器
- 容器分为 `主轴` 和 `交叉轴`
- `主轴` 为项目排列的轴线
- `交叉轴` 为项目对齐的轴线
- `flex布局` 会忽略容器的以下属性：`float`、`clear` 和 `vertical-align`
- 容器总共有6个属性

| 属性            | 说明                                                          |
| --------------- | ------------------------------------------------------------- |
| flex-direction  | 主轴的方向                                                    |
| flex-wrap       | 如果一条轴线排不下，如何换行                                  |
| flex-flow       | `flex-direction` 和 `flex-wrap` 的简写形式，默认 `row nowrap` |
| justify-content | 项目在**主轴**上的对齐方式，主轴方向改变之后也随之改变        |
| align-items     | 项目在**交叉轴**上如何对齐，主轴方向改变之后也随之改变        |
| align-content   | 多根轴线的对齐方式，如果只有一根轴线，则忽略                  |

## 项目

- 容器的子元素称为项目
- 项目共有6个属性

| 属性        | 说明                                                                        |
| ----------- | --------------------------------------------------------------------------- |
| order       | 排列顺序，越小越靠前，默认为0                                               |
| flex-grow   | 存在剩余空间，项目放大比例，默认为1                                         |
| flex-shrink | 空间不足，项目缩小比例                                                      |
| flex-basis  | 分配多余空间之前，项目占据的主轴空间                                        |
| flex        | `flex-grow` `flex-shrink` `flex-basis` 的组合属性                           |
| align-self  | 让单个子元素有不一样的对齐方式，覆盖 `align-items` 属性，默认auto继承父元素 |

### `flex-grow`

- 如果所有项目的`flex-grow`属性都为1，则它们将等分剩余空间。
- 如果一个项目的flex-grow属性为2，其他项目都为1，则前者占据的剩余空间将比其他项多一倍

### `flex-shrink`

- 如果所有项目的flex-shrink属性都为1，当空间不足时，都将等比例缩小
- 如果一个项目的flex-shrink属性为0，其他项目都为1，则空间不足时，前者不缩小。

### `flex-basis`

- 可以设定固定值，比如`300px`
