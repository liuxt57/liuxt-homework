# 仔细观察您洗衣机的运作过程，运用Top-down设计方法和Pseudocode 描述洗衣机控制程序。
假设洗衣机可执行的基本操作如下： 
water_in_switch(open_close)  // open 打开上水开关，close关闭

 water_out_switch(open_close)  // open 打开排水开关，close关闭 
 
 get_water_volume()  //返回洗衣机内部水的高度

motor_run(direction) // 电机转动。left左转，right右转，stop停 

time_counter()  // 返回当前时间计数，以秒为单位 

halt(returncode) //停机，success 成功 failure 失败

1）请使用伪代码分解“正常洗衣”程序的大步骤。包括注水、浸泡等 

1.获取模式要求数据

2.注水

3.浸泡

4.电机转动洗衣服

5.排水

6.脱水

7.关机



2）进一步用基本操作、控制语句（IF、FOR、WHILE等）、变量与表达式，写出每个步骤的伪代码 
```

READ hight,time1,time2        //1.获取模式要求数据

water_in_switch(open)         //2.注水
WHILE 水位<hight
ENDWHILE
waterinswitch(close)

浸泡                          //3.浸泡
WHILE 时间1<time1
ENDWHILE

WHILE 时间2<time2            //4.洗衣
motorun(left)
motorun(right)
ENDWHILE
motorun(stop)

WHILE 水位>0                 //5.排水
wateroutswitch(open)
ENDWHILE
wateroutswitch(close)

WHLILE 时间3<time3            //6.脱水
  motorrun(left)
  motorrun(right)
ENDWHILE
    motorrun(stop)

    halt(success)              //7.关机

```

3）根据你的实践，请分析“正常洗衣”与“快速洗衣”在用户目标和程序上的异同。 你认为是否存在改进（创新）空间，简单说明你的改进意见？ 

快速洗衣相较于正常洗衣要求的用时更短，因而没有浸泡的步骤。


4）通过步骤3），提取一些共性功能模块（函数），简化“正常洗衣”程序，使程序 变得更利于人类理解和修改维护。例如： wait(time) //等待指定的时间； 注水(volume,timeout) //在指定时间内完成注水，否则停机； 排水(timeout)。等子程序