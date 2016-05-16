# 2016_bop_semifinal
2016 bop senifinal python code 

进了决赛了，最终排名还没有出来就把代码放出来
复赛官方用例5组，不加缓存，成绩在49.975左右，一个用例的查询时间大概是120ms，每次查询academic api时间是70ms


## 加速的方法：
1. socket 长连接
2. 使用or and 语句查询拼接
3. 一个语句同时查询两次（单次查询时间波动较大，两次查询同时进行，并且使用先返回的结果，会更稳定）
4. 尽可能减少查询次数，AuId-AuId总共一次查询 其他情况总共两到三次串行查询


## 代码中遇到的问题等：
1. requests > urllib2 >httplib > socket长连接 时间消耗依次减少
2. 要是可以直接获得线程的结果就好了
3. @profile kernprof 可以查看每一行代码的运行时间，但不能看多线程中的部分。
4. flask 作为服务器很方便，效率不明。


<img alt="submission" src="https://github.com/dyslove123/2016_bop_semifinal/blob/master/rank.png" width="30%" height="30%">

