# 什么是时间戳
```
JavaScript时间戳：是指格林威治时间1970年01月01日00时00分00秒(北京时间1970年01月01日08时00分00秒)起至现在的总毫秒数。

Unix时间戳：是指格林威治时间1970年01月01日00时00分00秒(北京时间1970年01月01日08时00分00秒)起至现在的总秒数。
```

# JavaScript时间戳相互转换
## C# DateTime转换为JavaScript时间戳
``` c#
System.DateTime startTime = TimeZone.CurrentTimeZone.ToLocalTime(new System.DateTime(1970, 1, 1)); // 当地时区
long timeStamp = (long)(DateTime.Now - startTime).TotalMilliseconds; // 相差毫秒数
System.Console.WriteLine(timeStamp);
```

## JavaScript时间戳转换为C# DateTime
``` c#
long jsTimeStamp = 1478169023479;
System.DateTime startTime = TimeZone.CurrentTimeZone.ToLocalTime(new System.DateTime(1970, 1, 1)); // 当地时区
DateTime dt = startTime.AddMilliseconds(jsTimeStamp);
System.Console.WriteLine(dt.ToString("yyyy/MM/dd HH:mm:ss:ffff"));
```

# Unix时间戳相互转换
## C# DateTime转换为Unix时间戳
``` c#
System.DateTime startTime = TimeZone.CurrentTimeZone.ToLocalTime(new System.DateTime(1970, 1, 1)); // 当地时区
long timeStamp = (long)(DateTime.Now - startTime).TotalSeconds; // 相差秒数
System.Console.WriteLine(timeStamp);
```

## Unix时间戳转换为C# DateTime
``` c#
long unixTimeStamp = 1478162177;
System.DateTime startTime = TimeZone.CurrentTimeZone.ToLocalTime(new System.DateTime(1970, 1, 1)); // 当地时区
DateTime dt = startTime.AddSeconds(unixTimeStamp);
System.Console.WriteLine(dt.ToString("yyyy/MM/dd HH:mm:ss:ffff"));
```
