### 一、容器的属性

    1、display属性
    display: flex;父盒子默认100%
    display: inline-flex;父盒子会自动撑开

    2、flex-direction属性
    flex-direction: row;默认值 主轴为水平方向，起点在左端。
    flex-direction: row-reverse; 主轴在水平方向，起点在右端。
    flex-direction: column; 主轴为垂直方向，起点在上沿。
    flex-direction: reverse; 主轴为垂直方向，起点在下沿。

    3、flex-wrap属性
    在默认情况下，项目都是排在一条线（又称为轴线）上
    flex-wrap属性定义，如果一条轴线排不下，如何换行
    
    nowrap（默认）:不换行 压缩
    flex-wrap: nowrap;

    flex-wrap: wrap;换行，第一行在上方

    flex-wrap: reverse;换行，第一行在下方

    4、flex-flow属性
    是flex-direction属性和flex-wrap属性的简写形式，默认值为row nowrap

    5、justify-content属性(重点)
    justify-content属性是定义了项目在主轴上的对齐方式
    
    justify-content: flex-start;默认值（左对齐）

    justify-content: flex-end;右对齐

    justify-content: center;居中

    justify-content: space-between;两端对齐，项目之间的间隔都相等

    justify-content: space-around;每个项目两侧的间隔都相等，项目之间的间隔币项目与边框的间隔大一倍

    6、align-items属性
    align-items属性是定义项目在交叉轴上如何对齐的
    align-items: flex-start;交叉轴的起点对齐 
    align-items: flex-end;交叉轴的终点对齐
    align-items: center;交叉轴的中点对齐
    align-items: baseline;项目的第一行文字的基线对齐
    align-items: stretch;(默认值)如果项目未设置高度或者设置为auto，则将占满整个容器的高度

    7、align-content属性
    align-content属性定义了多根轴线在交叉轴上的对齐方式
    如果项目只有一根轴线（一行），则该属性不起作用
    flex-wrap: wrap;换行
    align-content: flex-start;多轴线对齐

    flex-wrap: wrap;
    align-content: flex-end;底部多轴线对齐

    flex-wrap: wrap;
    align-content: center;多行垂直居中

    flex-wrap: wrap;
    align-content: space-between;多行文字的两端对齐

    flex-wrap: wrap;
    align-content: space-around;每根周线两侧的间隔都相等。所以周线之间的间隔币轴线与边框的间隔大一倍

    flex-wrap: wrap;
    align-content:stretch(默认值)轴线沾满整个交叉轴