from  itertools import product
m_power = int(input())
prod = []
co_eff = []
for i in range(m_power):
    n,m = input().split(" ")
    prod.append(int(n))
    co_eff.append(int(m))

n_power = int(input())
prod1 = []
co_eff1 = []
for i in range(n_power):
    n,m = input().split(" ")
    prod1.append(int(n))
    co_eff1.append(int(m))

result_prod = list(product(prod,prod1))
result_co_eff = list(product(co_eff,co_eff1))
#print(result_prod)
d = {}
for i in range(len(result_prod)):
    g = result_prod[i][0] + result_prod[i][1]
    h = result_co_eff[i][0] * result_co_eff[i][1]
    if g not in d:
        d[g] = h
    else:
        d[g]+=h
d =  dict(sorted(d.items(),key = lambda x: -x[0]))

x = list(d.keys())
for i in range(len(x)):
    if d[x[i]] != 0 and i > 0:
        if d[x[i]] > 0:
            print(" + ",end="")
        else:
            print(" - ",end="")
    if d[x[i]] != 0:
        print(abs(d[x[i]]),end="")
    if d[x[i]] !=0 and x[i] !=0:
        print("x^{}".format(x[i]),end="")
