# Distance-and-Data-Searching

# Question-1
#1.A Robot moves in a Plane starting from the origin point (0,0).The robot can move UP,DOWN,LEFT,and RIGHT. 
#The trace of Robot movement is as given following:UP 5DOWN 3LEFT 3RIGHT 2(The numbers after 
#directions are steps) Write a program to compute the current distance from the origin point after sequencing
#of movements. Hint: Use the math module.


# Answer
import math

x, y =(0, 0)

while True:
   t = input("Enter the step number : ")
   if t == "":
       break

   else:
       t = t.split(".") 

       if t[0] == "up_side":
           y += int(t[1])
       elif t[0] == "down_side":
           y-= int(t[1])
       elif t[0] == "left_side":
           x -= int(t[1])
       elif t[0] == "right_side":
           x+= int(t[1])

f = math.sqrt(x**2 + y**2)

print("Distance travelled by the robot:", f)




#Question-2
#Data of XYZ company is stored in a sorted list. Write a program to search for specific data 
#from that list.Hint:Use if/elif to deal with conditions.


#Answer
s = input("Enter the elements ")
ele = input("Enter the elements which we want: ")

eles = str(s).split(";")

if ele in eles:
    print(f"{ele} is present in given list at position {eles.index(ele)+1}")
else:
    print(f"{ele} is not present ")
