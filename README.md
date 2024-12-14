# Bubble-and-Selection-sort
Program to implement bubble and selection sort
def Bubble_sort(a,n):
	for i in range (n-1):
		for j in range (n-i-1):
			if (a[j] > a[j+1]):
				temp=a[j]
				a[j]=a[j+1]
				a[j+1]=temp
	print("\nPass ",a,end=",")
	
#<******************************************************>

def Selection_sort(a,n):
	for i in range(n-1):
		min=i
		for j in range (i+1,n):
			if (a[j] < a[min]):
				min=j
		(a[i],a[min])=(a[min],a[i])
	print("\nPass ",a,end=",")
	
#<******************************************************>

n=int(input("\nEnter Total number of students in First year:\n"))
print("\n---------First year percentage of students----------\n")
a=[]
for i in range(n):
	empt=float(input())
	a.append(empt)

flag=1
while(flag==1):
	print("\n------------------------MENU-----------------------\n")
	
	print("1.Bubble sort")
	print("2.Selection sort")
	print("3.Exit")
	
	ch=int(input("\nEnter your choice from 1 to 3:\n"))
	
	if ch==1:
		Bubble_sort(a,n)
	elif ch==2:
		Selection_sort(a,n)
	elif ch==3:
		flag=0
		print("Thanks for using this program!!!\n")
	else:
		print("Wrong choice!!!\n")
		a=input("\n Do you want to continue (yes/no):\n")
		if a=="yes":
			flag=1
		else:
			flag=0
			print("Thanks for using this program!!!\n")

