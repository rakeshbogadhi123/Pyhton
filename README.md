# Pyhton
Python Learning


n=int(input())
dic1={}
value=0
count=0
dic3={}

for i in range(n):
    a=0
    b=0
    a,b=input().split(' ')
    dic1.update({a:int(b)})
dic1=sorted(dic1.items(),key=lambda x:x[0],reverse=True)
#print(dic1)
m=int(input())
dic2={}
for i in range(m):
    x=0
    y=0
    x,y=input().split(' ')
    dic2.update({x:int(y)})
dic2=sorted(dic2.items(),key=lambda x:x[0],reverse=True)
dic2=dict(dic2)
dic1=dict(dic1)

#print(dic1)
#print(dic2)

#print(dic3)
p=max(n,m)
count1=0
count2=0
count3=0
#print(a-1)

        
        
for i in dic1.keys():
    dic3.update({i:dic1[i]})
for i in dic2.keys():
    if i in dic3:
        s=dic3[i]+dic2[i]
        dic3.update({i:s})
    else:
        dic3.update({i:dic2[i]})
    
    
    
        
#print(dic3)
dic3=sorted(dic3.items(),key=lambda x:x[0],reverse=True)
#print(dic3)
for k,v in dic3:
    if v==0:
        count=count+1
    elif v>0 :
        if count1==0 and p==1 and v==1 and int(k)==1:
            count3+=1
            print(f'x',end='')
        elif count1==0 and p==1 and v>1 and int(k)>1:
            print(f'{v}x^{k}',end='')
        elif count1==0  and v==1 and int(k)>1:
             print(f'x^{k}',end='')
         
            #print()
        elif v==1 and int(k)>1:
            count3+=1
            print(f' + x^{k}',end='')
        elif v==1 and int(k)==1:
            count3+=1
            print(f' + x',end='')
        elif v==1 and k==0:
            count3=count3+1
            print(f' + {v}',end='')
        elif count1==0 and p>1:
             count3+=1
             print(f'{v}x^{k}',end='')
            
        #if k>1 and k==a-1:
        #    print(f'{v}x^{k}',end='')
        elif int(k)>1 and int(k)<p-1:
            count3+=1
            print(f' + {v}x^{k}',end='')
        elif int(k)==1:
            count3+=1
            print(f' + {v}x',end='')
        elif int(k)==0:
            count3+=1
            print(f' + {v}',end='')
            
   
    elif v<0:
        v=v*-1
        if count2==0 and p==1 and v==1 and int(k)==1:
             count3+=1
             print(f'-x',end='')
        elif count2==0 and p==1 and v>1 and int(k)>1:
            print(f'-{v}x^{k}',end='')
        elif count2==0 and v==1 and int(k)>1:
            print(f'-x^{k}',end='')
          
             #print()
        elif v==1 and int(k)>1:
            print(f' - x^{k}',end='')
        elif v==1 and int(k)==1:
            print(f' -x',end='')
        elif v==1 and int(k)==0:
            print(f' - {v}',end='')
        elif count2==0 and p>1:
            count3+=1
            print(f'-{v}x^{k}',end='')
            
        #if k>1 and k==a-1:
         #   print(f'-{v}x^{k}',end='')
        elif int(k)>1 and int(k)<p-1:
            count3+=1
            print(f' - {v}x^{k}',end='')
        elif int(k)==1: 
            count3+=1
            print(f' - {v}x',end='')
        elif int(k)==0:
            count3+=1
            print(f' - {v}',end='')
    count2+=1
    count1+=1
if count!=0 and count3==0:
    print('0')
else:
    print()
