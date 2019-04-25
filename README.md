##  LitePager，一个轻量级的ViewPager，仿新版网易云歌单广场
### 博客详情： 敬请期待。。。

### 使用方式:
#### 添加依赖：
```
implementation 'com.wuyr:litepager:1.0.0'
```

### APIs:
|Method|Description|
|------|-----------|
|addViews(int... layouts)|批量添加子View|
|addViews(View... views)|批量添加子View|
|setSelection(View target)|选中指定子View|
|setSelection(int index)|根据索引选中子View|
|setOrientation(int orientation)|设置方向(默认: ORIENTATION_HORIZONTAL):<br>**ORIENTATION_HORIZONTAL**(水平)<br>**ORIENTATION_VERTICAL**(垂直)|
|setFlingDuration(long duration)|设置动画的时长|
|setMaxScale(float maxScale)|设置**最大**缩放比例|
|setMinScale(float minScale)|设置**最小**缩放比例|
|setMaxAlpha(float maxAlpha)|设置**最大**不透明度|
|setMinAlpha(float minAlpha)|设置**最小**不透明度|
|setOnScrollListener(OnScrollListener listener)|设置滚动状态监听:<br>**STATE_IDLE**(静止状态)<br>**STATE_DRAGGING_LEFT**(向左拖动)<br>**STATE_DRAGGING_RIGHT**(向右拖动)<br>**STATE_DRAGGING_TOP**(向上拖动)<br>**STATE_DRAGGING_BOTTOM**(向下拖动)<br>**STATE_SETTLING_LEFT**(向左调整)<br>**STATE_SETTLING_RIGHT**(向右调整)<br>**STATE_SETTLING_TOP**(向上调整)<br>**STATE_SETTLING_BOTTOM**(向下调整)<br>|
|setOnItemSelectedListener(SelectedListener listener) |设置子View被选中的监听|
|getSelectedChild() |获取当前选中的子View|

### Attributes:
|Name|Format|Description|
|----|-----|-----------|
|orientation|enum (默认: horizontal)<br>**horizontal**(水平)<br>**vertical**(垂直)|方向|
|flingDuration|integer (默认: 400)|动画时长|
|maxScale|float (默认: 1)|**最大**缩放比例|
|minScale|float (默认: 0.8)|**最小**缩放比例|
|maxAlpha|float (默认: 1)|**最大**不透明度|
|minAlpha|float (默认: 0.4)|**最小**不透明度|

### 添加子View方式：
#### XML

``` xml
    <com.wuyr.litepager.LitePager
        android:layout_width="match_parent"
        android:layout_height="wrap_content">

        <View
            android:layout_width="150dp"
            android:layout_height="200dp"
            android:background="#F00" />

        <View
            android:layout_width="150dp"
            android:layout_height="200dp"
            android:background="#0F0"/>

        <View
            android:layout_width="150dp"
            android:layout_height="200dp"
            android:background="#00F"/>
    </com.wuyr.litepager.LitePager>
```

#### 或者

``` java
    LitePager litePager = ...;
    View child1 = ...;
    View child2 = ...;
    View child3 = ...;
    //直接添加子View
    litePager.addViews(child1, child2, child3);
    
    //或者通过布局添加
    litePager.addViews(R.layout.view_child1, R.layout.view_child2, R.layout.view_child3);
```

<br>

### Demo下载: [app-debug.apk](https://github.com/wuyr/LitePager/raw/master/app-debug.apk)
### Demo源码地址： <https://github.com/wuyr/LitePager>

### 效果 (图1为网易云原效果)：
![preview](https://github.com/wuyr/LitePager/raw/master/previews/preview1.gif) ![preview](https://github.com/wuyr/LitePager/raw/master/previews/preview2.gif)
![preview](https://github.com/wuyr/LitePager/raw/master/previews/preview3.gif) ![preview](https://github.com/wuyr/LitePager/raw/master/previews/preview4.gif)
