---
title: 'Python 圆周率撒点计算'
date: 2024-07-23T08:56:23+08:00
draft: false
authors:
  - '元灏'
comment: true
description: '2024年7月23日'
tags: ['python']
toc: true
autoCollapseToc: true
---

## Python 圆周率撒点计算

浅浅的尝试一下

	from random import random
	from time import perf_counter
	import datetime
	import time

	l=0

	while True:

    	a=1000*1000
    	b=0.0
    	c=perf_counter()

    	for i in range(1,a+1):
        	x,y=random(),random()
        	d=pow(x **2 + y **2,0.5)
        	if d<=1.0:
            	b=b+1
    	e=4*(b/a)

    	print(e)
    	j=('--->{:.5f}s'.format(perf_counter()-c))
    
    	#time.sleep(1)

    

    	if l<=100 or e==3.141592:
        	l=l+1
        
        	print('--->',l,'<---')
        	if l>100 and e==3.141592:

            	print('write','5s')

            	time.sleep(5)

            	now=datetime.datetime.now()

            	p=(e,'---',l,'次')
            	file=open(r'D:\库\日志.txt',"a")
            	file.write(p)
            	file.close()

            	file=open(r'D:\库\日志.txt',"a")
            	file.write(now)
            	file.close()

            	break
## 效果不错

勉强能用

	PS D:\porgramming\vs code text> & D:/porgramming/Python/python.exe "d:/porgramming/vs code text/圆周率撒点.py"
	3.140468
	---> 1 <---
	3.140852
	---> 2 <---
	3.141784
	---> 3 <---
	3.140064
	---> 4 <---
	3.138836
	---> 5 <---
	3.139852
	---> 6 <---
	3.141596
	---> 7 <---
	3.142672
	---> 8 <---
	3.14244
	---> 9 <---
	3.141112
	---> 10 <---
	3.140224
	---> 11 <---
	3.1393
	---> 12 <---
	3.141048
	---> 13 <---
	3.144128
	---> 14 <---
	3.14364
	---> 15 <---
	3.142388
	---> 16 <---
	3.142024
	---> 17 <---
	3.141652
	---> 18 <---
	3.138428
	---> 19 <---
	3.141784
	---> 20 <---
	3.141332
	---> 21 <---
	3.141176
	---> 22 <---
	3.138412
	---> 23 <---