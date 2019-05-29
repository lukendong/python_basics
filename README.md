# python_basics
python大神正在路上  

# case1.九九乘法表输出 
for语句
for i in range (1,10):  
    for j in range(1,10):  
        print(j,'X',i,'=',j*i,end=' ')  
        if j==i:  
            print('\n')  
            break  
while语句
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
while语句
i=0  
while i<20:  
    i=i+1  
    print(' '*(21-i),'*'*(2*i-1))   
for语句
for i in range(1,21):  
    print(' '*(21-i),"*"*(2*i-1),' '*(21-i))  
    
# case3.1234组合多少不重复的三位数分别输出 
for语句例1
num=0              
for i in range(1,5):        
    for j in range(1,5):        
        for n in range(1,5):        
            if (i!=j)and(i!=n)and(j!=n):        
                print(i,j,n)        
                num=num+1       
print("共有",num,"个数")        
for语句例2
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

# case5.一个整数，它加上100后是一个完全平方数，再加上168又是一个完全平方数，请问该数是多少？
分析：(x+1)的平方-x的平方即2*X+1<=100,才可能加上100后被1个数完全平方，所以x肯定50内，不需要把数字弄的过大，增加计算      
for x in range(1,50):       
    for i in range(1,100):      
        for j in range(1,100):      
            if x+100==i*i and x+100+168==j*j:       
                print(x)        

# case6.题目：输入任意整数（不多于10个），请把这些数由小到大输出       
m=[]                
print("这是一个输入整数比较大小的程序，最多输入10个")                
for i in range(1,11):       
    print("请输入第",i,"个数")        
    xi=int(input())     
    m.append(xi)        
    print("是否继续输入:","输入n终止继续输入，否则任意继续输入")       
    yn =input()     
    if yn =='n':        
        break       
m.sort()        
for j in m:     
    print(j, end=' ')       
    
#case7.题目：中国有34个省会城市，要求打印20份试题问卷，要求每份都不一样？类似题目示例：请问**的省会城市是什么？正确答案与其余省会城市组成选项       
#创建字典集，类似题库     
def testexam(n):        
    import random       
    import os       
    maincity={'江苏':'南京','浙江':'杭州','湖北':'武汉','湖南':'长沙','山东':'济南','陕西':'西安','黑龙江':'哈尔滨',
          '吉林':'长春','辽宁':'沈阳','内蒙古':'呼和浩特','河北':'石家庄','新疆':'乌鲁木齐','甘肃':'兰州',
          '青海':'西宁','宁夏':'银川','河南':'郑州','山西':'太原','安徽':'合肥','四川':'成都','贵州':'贵阳',
          '上海':'上海','北京':'北京','天津':'天津','重庆':'重庆','云南':'昆明','广西':'南宁','西藏':'拉萨',
          '江西':'南昌','广东':'广州','福建':'福州','台湾':'台北','海南':'海口','香港':'香港','澳门':'澳门'}        
    cho_abc=['A','B','C','D']       
    ans=[]      
#创建试题       
    anspaper=open('C:\\Users\\Luken\\Desktop\\testexam\\anspaper.txt','w')      
    for exam_num in range(1,n+1):       
#打开要创建的试卷、答案目录，若没有则创建       
        exampaper=open('C:\\Users\\Luken\\Desktop\\testexam\\exampaper%s.txt' %(exam_num),'w')      
        exampaper.write('name:\n\n')        
        exampaper.write('class:\n\n')       
        main=maincity.keys()        
        main=list(main)     
        city=maincity.values()      
        city=list(city)     
        for ques_num in range(1,21):        
            p=main[random.randint(0,34-ques_num)]       
            exampaper.write( '%s、请问%s的省会城市是什么?\n' %(ques_num,p))        
            main.remove(p)      
            ans.append(maincity[p])     
            city.remove(maincity[p])        
            ans=ans+random.sample(city,3)       
            random.shuffle(ans)     
            for cho_num in range(4):        
                exampaper.write('%s、%s\n' %(cho_abc[cho_num],ans[cho_num]))            
            rightans=cho_abc[ans.index(maincity[p])]        
            anspaper.write(rightans)        
            ans=[]      
        anspaper.write('\n')        
        exampaper.close()       
    anspaper.close()        
                
print("请输入您要创建的试卷份数:")      
n=int(input())      
testexam(n)     

#case8.题目：找出10000以内的所有质数        
#分析：把素数2作为特例拿出来，事先定义素数个数x为1     
print(2,end='\t')       
m=[]        
x=1     
for i in range(3,10001):        
    for j in range(2,i):        
        m.append(i%j)       
        if j==i-1:      
            if 0 not in m:      
                x+=1        
                print(i,end='\t')       
                if x%20==0:     
                    print()     
    m=[]        

#case9.斐波纳契数列     
def f(i):       
    x=[]        
    for j in range(1,i+1):      
        if j<3:     
            x.append(1)     
            print(x[j-1],end="\t")      
        else:       
            x.append(x[j-3]+x[j-2])     
            print(x[j-1],end="\t")      
            if (j+2)%20==0:     
                print("\n")     
print("请输入要看到多少个数的:")       
n=int(input())      
f(n)        
