# Linear Search and Binary search
## Aim:
To write a program to perform linear search and binary search using python programming.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
## Linear Search:
1.	Start from the leftmost element of array[] and compare k with each element of array[] one by one.
2.	If k matches with an element in array[] , return the index.
3.	If k doesn’t match with any of elements in array[], return -1 or element not found.
## Binary Search:
1.	Set two pointers low and high at the lowest and the highest positions respectively.
2.	Find the middle element mid of the array ie. arr[(low + high)/2]
3.	If x == mid, then return mid.Else, compare the element to be searched with m.
4.	If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.
5.	Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
6.	Repeat steps 2 to 5 until low meets high
## Program:
i)	#Use a linear search method to match the item in a list.
```
###Program to search the item in given list using linear search
###Devoloped by: KATHIRESAN K
###Reg.no:212223110021
```
```

def search(array,key,n):
    for i in range(0,n):
        if key==array[i]:
            return i
            
    return -1
array=eval(input())
key=int(input())
array.sort()
n=len(array)
print(array)
result=search(array,key,n)
if result==-1:
    print("Element not found")
else:
    print("Element found at index: ",search(array,key,n))
```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
###Program to search the item in given list using Binary search
###Devoloped by: KATHIRESAN K
###Reg.no:212223110021
```
```
def binary(array,key,low,high):
    while(low<=high):
        mid=low+(high-low)//2
        if array[mid]==key:
            return mid
        elif array[mid]<key:
                low=mid+1
        elif array[mid]>key:
            high=mid-1
    return -1
array=eval(input())
key=int(input())
array.sort()
low,high=0,len(array)-1
print(array)
result=binary(array,key,low,high)
if result==-1:
    print("Element not found")
else:
    print("Element found at index: ",binary(array,key,low,high))
```
iii)	# Find the element in a list using Binary Search (recursive Method).

```
###Program to search the item in given list using Binary search(Recursive)
###Devoloped by: KATHIRESAN K
###Reg.no:212223110021
```
```
def binary(array,key,low,high):
    if high>=low:
        mid=low+(high-low)//2
        if array[mid]==key:
            return mid
        elif array[mid]<key:
                return binary(array,key,mid+1,high)
        elif array[mid]>key:
            return binary(array,key,low,mid-1)
    return -1
array=eval(input())
key=int(input())
array.sort()
low,high=0,len(array)-1
print(array)
result=binary(array,key,low,high)
if result==-1:
    print("Element not found")
else:
    print("Element found at index: ",binary(array,key,low,high))
```
## Sample Input and Output
###linear_search
![image](https://github.com/Kathiresan-23013376/Search-Algorithms/assets/150008375/0c4e461e-a0a6-4c12-9d85-b35e9a6fda2e)

###binary_search
![image](https://github.com/Kathiresan-23013376/Search-Algorithms/assets/150008375/c19c62b9-9844-4b22-805a-1a9a2ca7d35b)
###binary_search(using recursive function)


![image](https://github.com/Kathiresan-23013376/Search-Algorithms/assets/150008375/3afb0686-b0cd-4ba2-939c-78de87c8f552)



## Result
Thus the linear search and binary search algorithm is implemented using python programming.
