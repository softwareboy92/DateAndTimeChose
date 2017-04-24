        //这里根据你个人的需要进行设置，可以设置年月日or 年月日时分秒or 等等
TimeSelector  timeSelector = new TimeSelector(this, new TimeSelector.ResultHandler() {
     @Override
     public void handle(String time) {
                Toast.makeText(getApplicationContext(), "chose time ："+ time, Toast.LENGTH_SHORT).show();
            }
        }, "1900-12-31 23:59:00", "2100-12-31 23:59:00");

        timeSelector.setScrollUnit(TimeSelector.SCROLLTYPE.YEAR, 
        	TimeSelector.SCROLLTYPE.MONTH, 
        	TimeSelector.SCROLLTYPE.DAY,
        	 TimeSelector.SCROLLTYPE.HOUR, 
        	 TimeSelector.SCROLLTYPE.MINUTE);
        
//在style中需要的样式

     <style name="time_dialog" parent="android:style/Theme.Dialog">
        <item name="android:windowFrame">@null</item>
        <item name="android:windowNoTitle">true</item>
        <item name="android:windowIsFloating">true</item>
        <item name="android:windowContentOverlay">@null</item>
        <item name="android:windowBackground">@color/white</item>
    </style>

//在布局文件中需要的文件

<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical">

    <LinearLayout
        android:layout_width="fill_parent"
        android:layout_height="wrap_content"
        android:orientation="vertical">

        <RelativeLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:background="#ffffff"
            android:padding="10dp">

            <TextView
                android:id="@+id/tv_cancle"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_centerVertical="true"
                android:padding="10dp"
                android:text="取消"
                android:textColor="@color/colorPrimary"
                android:textSize="16sp" />


            <TextView
                android:id="@+id/tv_year"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_centerInParent="true"
                android:text="请选择时间"
                android:textColor="@color/colorPrimary"
                android:textSize="20sp" />


            <TextView
                android:id="@+id/tv_select"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_alignParentRight="true"
                android:layout_centerVertical="true"
                android:padding="10dp"
                android:text="选择"
                android:textColor="@color/colorPrimary"
                android:textSize="16sp" />

        </RelativeLayout>

        <View
            android:layout_width="fill_parent"
            android:layout_height="0.5dp"
            android:background="#11112233" />

        <RelativeLayout
            android:layout_width="fill_parent"
            android:layout_height="wrap_content">


            <LinearLayout
                android:layout_width="fill_parent"
                android:layout_height="wrap_content"
                android:layout_marginBottom="5dp"
                android:background="#ffffff"
                android:orientation="horizontal"
                android:paddingBottom="15dp"
                android:paddingLeft="20dp"
                android:paddingRight="20dp"
                android:paddingTop="15dp">

                <com.ant.control.timer.view.PickerView
                    android:id="@+id/year_pv"
                    android:layout_width="0dp"
                    android:layout_height="160dp"
                    android:layout_weight="3" />

                <TextView
                    android:layout_width="0dp"
                    android:layout_height="match_parent"
                    android:layout_weight="1"
                    android:gravity="center"
                    android:text="年"
                    android:textColor="#333333"
                    android:textSize="18sp" />

                <com.ant.control.timer.view.PickerView
                    android:id="@+id/month_pv"
                    android:layout_width="0dp"
                    android:layout_height="160dp"
                    android:layout_weight="2" />

                <TextView
                    android:layout_width="0dp"
                    android:layout_height="match_parent"
                    android:layout_weight="1"
                    android:gravity="center"
                    android:text="月"
                    android:textColor="#333333"
                    android:textSize="18sp" />

                <com.ant.control.timer.view.PickerView
                    android:id="@+id/day_pv"
                    android:layout_width="0dp"
                    android:layout_height="160dp"
                    android:layout_weight="2" />

                <TextView
                    android:layout_width="0dp"
                    android:layout_height="match_parent"
                    android:layout_weight="1"
                    android:gravity="center"
                    android:text="日"
                    android:textColor="#333333"
                    android:textSize="18sp" />

                <com.ant.control.timer.view.PickerView
                    android:id="@+id/hour_pv"
                    android:layout_width="0dp"
                    android:layout_height="160dp"
                    android:layout_weight="2" />

                <TextView
                    android:layout_width="0dp"
                    android:layout_height="match_parent"
                    android:layout_weight="1"
                    android:gravity="center"
                    android:text="时"
                    android:textColor="#333333"
                    android:textSize="18sp" />

                <com.ant.control.timer.view.PickerView
                    android:id="@+id/minute_pv"
                    android:layout_width="0dp"
                    android:layout_height="160dp"
                    android:layout_weight="2" />

                <TextView
                    android:layout_width="0dp"
                    android:layout_height="match_parent"
                    android:layout_weight="1"
                    android:gravity="center"
                    android:text="分"
                    android:textColor="#333333"
                    android:textSize="18sp" />
            </LinearLayout>


        </RelativeLayout>

    </LinearLayout>


</LinearLayout>