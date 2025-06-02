# 記述例

## Graphviz

### 図 3.1 無向グラフ

```graphviz
graph {
    rankdir="LR";
    node [shape=box];
    高校 -- 生徒;
    大学 -- 学生; 
}
```

### 図 3.2 有向グラフ(単方向)

```graphviz
digraph {
    rankdir="LR";
    node [shape=box];
    雨 -> 曇り;
    寝坊 -> 遅刻;
}
```

### 図 3.3 有向グラフ(双方向)

```graphviz
digraph {
    rankdir="LR";
    node [shape=box];
    日本 -> 中国;
    中国 -> 日本;
    商店 -> 客;
    客 -> 商店;
    D企業 -> S企業 [dir=both];
}
```

### 図 3.4 関係図

```graphviz
digraph {
    rankdir="LR";
    node [shape=box];

    Note1 [label="ノート1さつ\nのねだん\n□円"];
    Note5 [label="ノート5さつ\nのねだん\n□円"];
    Total [label="全部のねだん\n\n710円"];
    
    Note1 -> Note5 [label="5倍する"];
    Note1 -> Note5 [style=invis];
    Note5 -> Note1 [label="5でわる"];

    Note5-> Total [label="110をたす"];
    Note5-> Total [style=invis];
    Total -> Note5 [label="110をひく"];
}
```

### 図 3.5 WBS

```plantUML
@startwbs uml01
* UML 2.0 
** 構造に関する表記
*** クラス図
*** オブジェクト図
*** パッケージ図

@endwbs
```
