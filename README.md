# python_basics
python大神正在路上  

# case1.九九乘法表输出 
# for语句
for i in range (1,10):  
    for j in range(1,10):  
        print(j,'X',i,'=',j*i,end=' ')  
        if j==i:  
            print('\n')  
            break  
# while语句
i=0  
while i<9:  
    i=i+1  
    j=0  
    while j < i:  
        j=j+1  
        print(j,'X',i,'=',j*i,end='  ')  
        if j==i:  
            print('\n')  
            break  
        
# case2.树状输出  
# while语句
i=0  
while i<20:  
    i=i+1  
    print(' '*(21-i),'*'*(2*i-1))   
# for语句
for i in range(1,21):  
    print(' '*(21-i),"*"*(2*i-1),' '*(21-i))  
    
# case3.1234组合多少不重复的三位数分别输出 
# for语句例1
num=0
for i in range(1,5):
    for j in range(1,5):
        for n in range(1,5):
            if (i!=j)and(i!=n)and(j!=n):
                print(i,j,n)
                num=num+1
print("共有",num,"个数")
# for语句例2
m=[1,2,3,4]  
n=0  
for i in m:  
        for j in m:  
            for k in m:  
                if len({i,j,k})==3:  
                    print(100*i+j*10+k)  
                    n=n+1  
print("能组成",n ,"个无重复数字")  

# case4.输入某年某月某日，判断这一天是这一年的第几天？
while True:  
    print('请输入年份:')  
    y=int(input())  
    print("请输入月份:")  
    m=int(input())  
    if m<1 or m>12:  
        print("您输入的月份有误，请重新输入")  
    if 1<=m<=12:  
        print("请输入日:")  
        d=int(input())  
        if d<1 or d>31:  
                print("您输入的天数有误，请重新输入")  
        if m==1 or m==3 or m==5 or m==7 or m==8 or m==10 or m==12:  
            if 1<=d<=31:  
                break  
        if m==4 or m==6 or m==9 or m==11:  
            if 1<=d<=30:  
                break  
        if m==2:  
            if y%4==0:  
                if 1<=d<=29:  
                    break  
            if y%4!=0:  
                if 1<=d<=28:  
                    break  
print("nice，你输入的日期为",[y,m,d])  
if y%4==0:  
    if m==1:  
        s=d  
    if m==2:    
        s=31+d    
    if m==3:    
        s=31+29+d   
    if m==4:    
        s=31+29+31+d    
    if m==5:    
        s=31+29+31+30+d   
    if m==6:    
        s=31+29+31+30+31+d    
    if m==7:    
        s=31+29+31+30+31+30+d   
    if m==8:    
        s=31+29+31+30+31+30+31+d    
    if m==9:    
        s=31+29+31+30+31+30+31+31+d   
    if m==10:   
        s=31+29+31+30+31+30+31+31+30+d    
    if m==11:   
        s=31+29+31+30+31+30+31+31+30+31+d   
    if m==12:   
        s=31+29+31+30+31+30+31+31+30+31+30+d    
if y%4!=0:    
    if m==1:    
        s=d   
    if m==2:    
        s=31+d    
    if m==3:    
        s=31+28+d   
    if m==4:    
        s=31+28+31+d    
    if m==5:    
        s=31+28+31+30+d   
    if m==6:    
        s=31+28+31+30+31+d    
    if m==7:    
        s=31+28+31+30+31+30+d   
    if m==8:    
        s=31+28+31+30+31+30+31+d    
    if m==9:    
        s=31+28+31+30+31+30+31+31+d   
    if m==10:   
        s=31+28+31+30+31+30+31+31+30+d    
    if m==11:   
        s=31+28+31+30+31+30+31+31+30+31+d   
    if m==12:   
        s=31+28+31+30+31+30+31+31+30+31+30+d    
print('您输入的日期为第',s,"天")   

 
