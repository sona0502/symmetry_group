import matplotlib
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt

print("Enter the name of shape on which you wont to perfrom operation:")
print("1.equilateral triangle")
print("2.square")
print("3.hexagon")
print("4.exit")

shape = input("Enter your input: ") 
print(shape) 

        
class differentshape:
    def switch(self, shape):
            default = "Invalid shape"
            return getattr(self, 'case_' + str(shape), lambda: default)()
    def case_1(self):
        return "Equilateral triangle"
    def case_2(self):
        return "square"
    def case_3(self):
        return "hexagon"

s = differentshape()

print(s.switch(shape))




class shapes:
    
  def __init__(self):
        self.X = []
        self.Y = []
        self.labels = []
        self.shape=""
        
  def getDataFrame(self):
        points=pd.DataFrame({"X":self.X,"Y":self.Y,"labels":self.labels})
        points=points.append(points.iloc[0])
        return points
    
    
 def triangle(self):
        self.X = [0,3,1.5]
        self.Y = [0,0,3]
        self.labels = ["A","B","C"]
        self.shape="triangle"
        return self.getDataFrame()

   
  def square(self):
        self.X = [0,2,2,0]
        self.Y = [0,0,2,2]
        self.labels = ["A","B","C","D"]
        self.shape="square"
        return self.getDataFrame()


 def hexagon(self):
        self.X = [0,1,1,0,-1,-1,0]
        self.Y = [0,1,2,3,2,1,0]
        self.labels = ["A","B","C","D","E","F"]
        self.shape="hexagon"
        return self.getDataFrame()
    
A = [0,0]
B = [1,1]
C = [1,2]
D = [0,3]
E = [-1,2]
F = [-1,1]
X = [0,1,1,0,-1,-1,0]
Y = [0,1,2,3,2,1,0]

points=pd.DataFrame({"X":X,"Y":Y})


def show(labels):
    plt.figure(figsize=(6,6))
    plt.plot(points.X,points.Y)
    plt.title('Symmetries of Hexagon')
    plt.xlabel('x axis')
    plt.ylabel('y axis')
    for index,point in enumerate(labels):
        plt.scatter(points.X[index],points.Y[index])
        plt.annotate(point, # this is the text
                 (points.X[index],points.Y[index]), # this is the point to label
                 textcoords="offset points", # how to position the text
                 xytext=(0,7)) # distance from text to points (x,y)
               


labels=["A (0,0)","B(1,1)","C(1,2)","D(0,3)","E(-1,2)","F(-1,1)"]

print ("identity" )
show(labels)
print("Enter what type of symmetry you wont:")
print("1.identity")    # E
print("2. proper rotation")    #through an angle theta
print("3.reflection")  #across a line
print("4. inverion")   #through a point 
print("5.exit")
symmetry = input("Enter your input: ") 
print(symmetry) 



class differentsymmetry:
    def switch(self, symmetry):
            default = "Invalid symmetry operation"
            return getattr(self, 'case_' + str(symmetry), lambda: default)()
    def case_1(self):
        return "identity"
    def case_2(self):
        return "proper rotation"
    def case_3(self):
        return "reflection"
    def case_4(self):
        return "inversion"
s = differentsymmetry()
print(s.switch(symmetry))

user_input = True
while user_input:
    validInput = False
    while not validInput:
        # Get user input
			try:
            
  operation = int(input("What do you want to continue this?\n 1. identity,\n 2. proper rotation,\n 3. reflection,\n 4.inversion.\n Enter number:"))
            validInput = True
        except:
            print("Invalid Input. Please try again.")
    if(operation == 1):
        print("operation identity proceed further")
    elif(operation == 2):
        print("operation proper rotation proceed further")
    elif(operation == 3):
         print("operation reflection proceed further")
    elif(operation == 4):
        print("operation inversion proceed further")
    else:
        print("I don't understand. Please try again.")
    user_yn = input('Would you like to do another calculation? ("y" for yes or any other value to exit.)')
   if(user_yn == 'y'):
        if(operation== 1):
                print("1.identity")    # E
                print("enter the angle of rotation")
                print("1.zero degree")
                print("2.360 degree")
                angle = input("enter your input")
                print(angle)
        
   elif(operation == 2):
                print("2. proper rotation")    
                print("enter the angle of rotation ")
                print("1. zero degree")
                print ("2. 60 drgee")
                print("3. 90 degree")
                print("4. 120 degree") 
                print("5. 180 degree")
                print("6. 240 degree") 
                print( "7. 270 degree")
                print("8.300 degree")
                print("9.  360  degree")
                angle = input("enter your input")
                print(angle)
        elif(operation == 3):
                print("3. reflection")    
                print("enter the line of reflection ")
                print("1. line parallel to x axis")
                print("2. line parallel to y axis")
                print("3. line passing through origin")
                
  line = input("enter your input")
  print(line)
  else:
        break
				
def show():
    plt.figure(figsize=(6,6))
    plt.plot(points.X,points.Y)
    plt.title('symmetry of different shapes')
    plt.xlabel('x axis')
    plt.ylabel('y axis')
# Its for printing the labels and numbers on the graph
   for index,point in enumerate(points[:-1].labels):
        plt.scatter(points.X[index],points.Y[index])
        plt.annotate(point+"("+str(points.X.iloc[index])+","+str(points.Y.iloc[index])+")", # this is the text
                 (points.X.iloc[index],points.Y.iloc[index]), # this is the point to label
                 textcoords="offset points", # how to position the text
                 xytext=(0,6), # distance from text to points (x,y)
                 ha='center')




class operationReflectionT:
    
    # For triangles reflection with X keeping index zero constant
   def keepXContant(points):
        _temp=points.labels.iloc[1];
        points.labels.iloc[1]=points.labels.iloc[2];
        points.labels.iloc[2]=_temp
        points.iloc[points.shape[0]-1]=points.iloc[0]
        return points
        
    # For triangles keep second cord as it is
   def keepYContant(points):
        _temp=points.labels.iloc[0];
        points.labels.iloc[0]=points.labels.iloc[2];
        points.labels.iloc[2]=_temp
        return points
    
    # For triangles
   def keepZContant(points):
        _temp=points.labels.iloc[0];
        points.labels.iloc[0]=points.labels.iloc[1];
        points.labels.iloc[1]=_temp
        return points

points=operationReflection.keepXContant(points)
show()

class operationRotation:
    def rotate90Degree(points):
        for index in range(0,points.shape[0]-1):
            points.labels.iloc[index]=points.labels.iloc[index+1]
            points.labels.iloc[points.shape[0]+1]=points.labels.iloc[0]
            return points

   def rotate180Degree(points):
        points=rotate180Degree(points)
        return points
    
   def rotate270Degree(points):
        points=rotate180Degree(points)
        return points
    
   def rotate360Degree(points):
        points=rotate270Degree(points)
        return points

new=shapes()
points=new.triangle()
show()


new=shapes()
points=new.square()
show()

new=shapes()
points=new.hexagon()
show()

points=operationRotation.rotate90Degree(points)
show()

points=operationReflectionT.keepXContant(points)
print("reflection in a plane passing through diagonal one")
show()

points=operationReflection.keepXContant(points)
show()








        

    
