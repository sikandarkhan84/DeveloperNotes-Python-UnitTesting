[Self Keyword](https://www.geeksforgeeks.org/self-in-python-class/#:~:text=self%20represents%20the%20instance%20of,you%20need%20to%20use%20self.)
___
self represents the instance of the class. By using the “self” keyword we can access the attributes and methods of the class in python. It binds the attributes with the given arguments.

The reason you need to use self. is because Python does not use the @ syntax to refer to instance attributes. Python decided to do methods in a way that makes the instance to which the method belongs be passed automatically, but not received automatically: the first parameter of methods is the instance the method is called on

#### Example
```
# Write Python3 code here 

class car(): 
	
	# init method or constructor 
	def __init__(self, model, color): 
		self.model = model 
		self.color = color 
		
	def show(self): 
		print("Model is", self.model ) 
		print("color is", self.color ) 
		
# both objects have different self which 
# contain their attributes 
audi = car("audi a4", "blue") 
ferrari = car("ferrari 488", "green") 

audi.show()	 # same output as car.show(audi) 
ferrari.show() # same output as car.show(ferrari) 

# Behind the scene, in every instance method 
# call, python sends the instances also with 
# that method call like car.show(audi) 
```
##### Output:
```
Model is audi a4
color is blue
Model is ferrari 488
color is green
```
#### note:Self is a convention and not a real python keyword
1. self is parameter in function and user can use another parameter name in place of it.But it is advisable to use self because it increase the readability of code.