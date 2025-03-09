import sys

#print ('hello world')
x = "bobbys boy"
print(x[0:6])

#to find the string length
x = "bobbys boy"
print(len(x))
#to find the place in character


#to find the find word
x = "bobbys boy"
print(x.find ('y'))

#list
courses_1  = ['history', 'maths','geography']
courses_2 =['science','new subject']
#courses.append('art')
#print (len(courses))
#print(courses[0:2])
#print(courses)
#courses.insert(0,'physical education')
#print (courses)
courses_1.insert (3,courses_2)
print(courses_1)

# list extend
courses_1  = ['history', 'maths','geography']
courses_2 =['science','new subject']
courses_1.extend (courses_2)
print(courses_1)

# list remove
courses_1  = ['history', 'maths','geography']
courses_1.remove ('maths')
print (courses_1)

#list popped
courses_1  = ['history', 'maths','geography']

courses_1.pop()	
print (courses_1)

#list popped until lastb value
courses_1  = ['history', 'maths','geography']
popped = courses_1.pop()	
print (popped)

#list reverse
courses_1  = ['history', 'maths','geography']
courses_1.reverse()
print (courses_1)


#list sort
courses_1  = ['history', 'maths','geography']
courses_1.sort()
print (courses_1)

#list sort ascending

numbers = [1,9,4,6,7,9]
numbers.sort()
print (numbers)

#list sort descending
numbers = [1,9,4,6,7,9]
numbers.sort(reverse = 'true')
print (numbers)

print (2**3)

# some constructor function for finding data type

name = "ADIL"

print (type(name))
print(isinstance(name, str))
print (type(name)==str)

# some concatenation 
firstname = "ADIL"
lastname = "khan"
fullname = firstname + " "+ lastname
print (fullname)
fullname += " md"
print (fullname)

# User onput


#new = input('please select the value: \n')

#print (new)

#print ("")

#playerchoice = input("enter your number ....\n 1 for roch\n 2 for paper \3 for scissor: \n\n")
#if playerchoice < 1 | playerchoice >3:
 #	('you must enter 1,2 or 3')

 #List in pthon
newuser = ['me','myself', 'mine']
print(newuser[-1])
print(newuser.index('mine'))
print(newuser[0:2])
print(newuser[1:-3])

newuser.append('my')
print (newuser)

newuser += ['for', 'ramiz']
print (newuser)

newuser.insert (0,'jimmy')
print (newuser)

newuser[1:3] =['junaid','sahil']
print (newuser)
newuser.remove('junaid')
print (newuser)

#to remove the last member in list we used pop function
print (newuser.pop())
print (newuser)
del newuser [1]
#use user.sort for sorting

# tuples
# tuples is like list but it cant be changed and need to use()

mytuple = (23,45, 'adil')

print (type(mytuple))

onemoretuple =tuple(('jassy', 'jane'))
print (onemoretuple)
#print (data.)

#dictionaries

Garden = {
	"celebration": "happy",
	"avenue": "new road"
}

print(Garden)


#new type of string defining
newgarden = dict(red="color", bike="adventure")

print(newgarden)


print (Garden.get("celebration"))

print (Garden.values())
print (Garden.keys())

#change of the valus in dict
Garden ["happy"] ="sorrow"
print (Garden)

#pop.tem used for last item removal

del Garden["celebration"]
print (Garden)

#sets
#num ={1,2,3,4,5,6}

#Loops

#newnum = 1

#while newnum < 99:
 
#	print (newnum)
 
#	if newnum ==5:

# 		break
 
#	newnum +=1


#newnum2 = 1

#while newnum2 < 5:

# 	print (newnum2)
 
#	if newnum ==5:
 
#		continue
 
#	newnum +=1

names =["dave","dane","don","dub"]
for x in names:
	print (names)

for x in "maschheussetsaadsa":
	print (x)
for x in range (0,100,2):
	print (x)


carbrand = ["toyota", "maruti", "tata", "mahindra"]
pros = ["fast", "reliable", "tensile strength", "acceleration"]

for x in carbrand:
    for y in pros:
        print(x + " " + y)

#functions
def hello():
	print (" sky height!")
  
hello()



def sum(num1, num2):
	print (num1 + num2)
sum(14,567)
sum(12,83)
sum(345,23)

#recursion
def  add_one (num):
	if (num >= 9):
		return num +1 

	total  = num + 1
	print (total)
	return add_one(total)

add_one (0)


#scope
name = "adil"
def greeting():
	print (name)
	greeting()

#closure is a function having access  to the scope of its parent

def parent_function(person):
    coins = 3

    def play_game():
        nonlocal coins
        if coins > 1:
            print(f"\n{person} has {coins} coins left.")
        elif coins == 1:
            print(f"\n{person} has {coins} coin left.")
        else:
            print(f"\n{person} has no coins left.")
        coins -= 1

    return play_game

tommy= parent_function ("Tommy")
jenny= parent_function ("jenny")

tommy()
jenny()
