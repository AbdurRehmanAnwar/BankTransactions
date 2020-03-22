
import os
from datetime import datetime, date
import random 

def accountInfo():
    list=[]
    account=[]
    f=open("sample.log", "r")
    f1=f.readlines() #    for line in in_file:
    f.close()
   
    for line in f1:
      if(line!="\n"):  
        list.append(line)
        split_string=line.split(':')
        temp = split_string[:0 + 1] 
        temp = ":".join(temp) 
        account.append(int(temp))

    account.sort(reverse=False)
    updatedList=[]
    uniqueAccount=[]
    for value in account:
     for line in list:
       if(line!="\n"):
        split_string=line.split(':')
        temp = split_string[:0 + 1] 
        temp = ":".join(temp) 
        temp=int(temp)
        if temp==value and temp not in uniqueAccount:
           uniqueAccount.append(temp)
           updatedList.append(line)
           break   
        else:
          continue   
    while True:

     count=1
     for line in updatedList:
       split_string=line.split(':')
       number = split_string[:0 + 2] 
       temp=str(count)+")"
       print(temp,number[1],' ',end='')
       print(number[0])
       count+=1
     print("q)uit")
     count-=1
     choice=input("Enter choice => ")
     if(choice=='q'):
       break
     elif(choice.isdigit()):
        temp=int(choice)
        if(temp <=len(updatedList)):
          index=temp-1
          new=updatedList[index]
          print(new)
          new=new.split(':')
          detail= new[:0 + 5]
          print("account #: ",detail[0])
          print("name :",detail[1])
          print("balance: $",detail[4])

        else:
          print("This account holder does not exist ")
          continue
     else:
        print("Invalid Input\n")
        continue

    
    
   
def history():
    
    list=[]
    account=[]
    f=open("sample.log", "r")
    f1=f.readlines() #    for line in in_file:
    f.close()
   
    for line in f1:
      if(line!="\n"):  
        list.append(line)
        split_string=line.split(':')
        temp = split_string[:0 + 1] 
        temp = ":".join(temp) 
        account.append(int(temp))

    account.sort(reverse=False)
    updatedList=[]
    uniqueAccount=[]
    for value in account:
     for line in list:
       if(line!="\n"): 
        split_string=line.split(':')
        temp = split_string[:0 + 1] 
        temp = ":".join(temp) 
        temp=int(temp)
        
        if temp==value and temp not in uniqueAccount:
           uniqueAccount.append(temp)
           updatedList.append(line)
           break   
        else:
          continue
    
    while True:
     print("\nHistory")
     print("------")
     count=1
     for line in updatedList:
      split_string=line.split(':')
      number = split_string[:0 + 2] 
      temp=str(count)+")"
      print(temp,number[1],' ',end='')
      print(number[0])
      count+=1
     print("q)uit")
     count-=1

    

     choice=input("Enter choice => ")
     if(choice=='q'):
        break
     elif(choice.isdigit()):
        temp=int(choice)
        if(temp <=len(updatedList)):
          index=temp-1
          new=updatedList[index]
          new=new.split(':')
          detail= new[:0 + 1]
          detail = ":".join(detail)
          detail=int(detail)
          for line in list:
            if(line!="\n"): 
             split_string=line.split(':')
             temp = split_string[:0 + 1] 
             temp = ":".join(temp) 
             temp=int(temp)
             
             if(temp==detail):
               line=line.split(':')
               line= line[:0 + 5]
               print(line[2],end='')
               if(line[3]=="D"):
                 print(" deposit",end='')
               else:
                 print(" withdrawl",end='')
               print(" $",line[4])  
               
        else:
          print("This account holder does not exist ")
          continue
     else:
        print("Invalid Input\n")
        continue

    

def inserttransaction():
    print("\nInsert Transaction")
    print("------")
     
    print("create a new account ")
    list=[]
    account=[]
    f=open("sample.log", "r")
    f1=f.readlines() #    for line in in_file:
    f.close()

    for line in f1:

        list.append(line)
        split_string=line.split(':')
        temp = split_string[:0 + 1] 
        temp = ":".join(temp)
        if temp!="\n":
         temp=int((temp))
         account.append(temp)
    
    
    while True:

     damage=random.randint(1000,9999)
     print("account number is ",damage) 
     if(damage in account):
       print("account # already exits")
       continue
     else:
       break
               
    name=input("enter the name => ")
    Type=input("w for withdrawal or d for deposit =>")
    Type=Type.upper()
    amount=input("enter the amount =>")
    today=datetime.now().strftime("%y.%m.%d")
    string=str(damage)+":"+name+":"+today+":"+Type+":"+str(amount)+"\n"
    ff=open("sample.log", "a+")
    ff.write(string)
    ff.close()

if __name__== "__main__": 
  
  while True:
   option=input("account ")
   if(option=="-i"):
    accountInfo()
    break
   elif(option=="-h"):
    history()
    break 
   elif(option=="-t"):
    inserttransaction()
    continue
   elif(option=="?"):
    print("Usage\n----")
    print("Press -i for account info")
    print("Press -h for history")
    print("Press -t for insert transaction \n")
    break
   else:  
    print("Invalid Input")        
    break
