# DSL_pract.1
Welcome to my effort's rewards

def union(a,b):
    ans=a.copy()
    for i in a:
        if b not in a:
            ans.append(i)
    return ans

def intersection(a,b):
    ans=[]
    for i in a:
        if i in b:
            ans.append(i)
    return ans

def minus(a,b):
    ans=[]
    for i in a:
        if i not in b:
            ans.append(i)    
    return ans


while True:
    print("\nMenu:")
    print("1.Accept")  
    print("2.List of student who play both cricket and badminton ")
    print("3.List of students who play either cricket or badminton but not both")
    print("4.Number of students who play neither cricket nor badminton")
    print("5. Number of students who play cricket and football but not badminton")
    print("6. Exit") 
   

    choice = int(input("Enter your choice: "))

    if choice == 1:
        u=input("Enter the union list:").split(",")
        b=input("Enter the badminton list:").split(",")
        c=input("Enter the cricket list:").split(",")
        f=input("Enter the football list:").split(",")
        pass 
    elif choice == 2:
        print("List of student who play both cricket and badminton",intersection(b,c))
        pass
    elif choice == 3:
        print("List of students who play either cricket or badminton but not both",union((minus(c,intersection(b,c))),minus(b,intersection(b,c))))
        pass
    elif choice == 4:
        print("Number of students who play neither cricket nor badminton",minus(minus(u,b),c))
        pass
    elif choice == 5:
        print("Number of students who play cricket and football but not badminton",minus(intersection(c,f),b))
        pass
    elif choice == 6:
        break
    else:
        print("Invalid choice. Please try again.")

print("Program exited. Have a great day!")
