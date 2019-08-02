### example
 


### attr

| name               e| format                   | des      |
|:-------------------|:-------------------------|:---------|
| switch_open_color  | color                    | 打开状态底部颜色 |
| switch_close_color | color                    | 关闭状态颜色   |
| switch_dot_color   | color                    | 滑块颜色     |
| switch_slidable    | boolean                  | 是否支持滑块滑动 |
| switch_dot_margin  | dimension                | 滑块margin |
| switch_checked     | boolean                  | 默认状态     |
| switch_shape       | enum(circular/rectangle) | 分圆头/矩形形状 |


### use

```xml
<com.peng.pswitch.PSwitchView
        android:id="@+id/view_switch1"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_margin="20dp"
        app:switch_checked="false"
        app:switch_close_color="#CDCBCF"
        app:switch_dot_color="#E91E63"
        app:switch_dot_margin="2dp"
        app:switch_open_color="#00BCD4"
        app:switch_shape="circular"
        app:switch_slidable="true" />
```

```
{
    ...
   
     mViewSwitch1.setOnSwitchCheckListener(new PSwitchView.SwitchCheckListener() {
        @Override
        public void onCheckedChanged(boolean isChecked) {
            Toast.makeText(MainActivity.this, "mViewSwitch1 切换:" + isChecked, Toast.LENGTH_SHORT).show();
        }
    });
    
    //状态设置, 以下方式都可以
    //mViewSwitch1.toggle();
    mViewSwitch1.setChecked(true);   

}
```