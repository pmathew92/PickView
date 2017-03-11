
Forked from https://github.com/brucetoo/PickView

# PickView
This is a helper lib for us to pick date or province like IOS system 
WheelView widget.
Added feature to pick time with WheelView Widget

#TimePicker
    
   ```java
            
         TimePickerPopWin timePickerPopWin=new TimePickerPopWin.Builder(MainActivity.this, new       TimePickerPopWin.OnTimePickListener() {
                    @Override
                    public void onTimePickCompleted(int hour, int minute, String AM_PM, String time) {
                        Toast.makeText(MainActivity.this, time, Toast.LENGTH_SHORT).show();
                    }
                }).textConfirm("CONFIRM")
                        .textCancel("CANCEL")
                        .btnTextSize(16)
                        .viewTextSize(25)
                        .colorCancel(Color.parseColor("#999999"))
                        .colorConfirm(Color.parseColor("#009900"))
                        .build();
                timePickerPopWin.showPopWin(MainActivity.this);
      
   ```

#DatePicker

```java

      DatePickerPopWin pickerPopWin = new DatePickerPopWin.Builder(MainActivity.this, new DatePickerPopWin.OnDatePickedListener() {
                          @Override
                          public void onDatePickCompleted(int year, int month, int day, String dateDesc) {
                              Toast.makeText(MainActivity.this, dateDesc, Toast.LENGTH_SHORT).show();
                          }
                       }).textConfirm("CONFIRM") //text of confirm button
                              .textCancel("CANCEL") //text of cancel button
                              .btnTextSize(16) // button text size
                              .viewTextSize(25) // pick view text size
                              .colorCancel(Color.parseColor("#999999")) //color of cancel button
                              .colorConfirm(Color.parseColor("#009900"))//color of confirm button
                              .minYear(1990) //min year in loop
                              .maxYear(2550) // max year in loop
                              .showDayMonthYear(true) // shows like dd mm yyyy (default is false) 
                              .dateChose("2013-11-11") // date chose when init popwindow
                              .build();
                              
                              
```

