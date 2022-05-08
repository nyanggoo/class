# class
 I post what I studied, when I was brushing up on professor's lecture.
python, spiral array code. use only for, while loop.
aa, A=[], []
N=int(input())
for i in range(1, N+1):
  for s in range(1,N+1):
    aa.append(s)
  A.append(aa)
  aa=[]
#print(A)  #A를 채우기 위해서 만든 코드

ga=1 
for s in range(0, N-2):
  
  for i in range(s, N-s):
    A[s][i]=ga
    ga+=1

  for i in range(s, N-1-s):
    if(i+1==N-s): break
    A[i+1][N-1-s]=ga
    ga+=1
#처음에 range(s+1,N-s) 했는데 로 하면 오류남.
  for i in range(s+1, N-s):
    A[N-1-s][N-i-1]=ga
    ga+=1
  
  for i in range(s+1, N-s-1):
    A[N-i-1][s]=ga
    ga+=1

print(A)
