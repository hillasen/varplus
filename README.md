Var+
=============
1. About
-------------
Varplus is a better way to use variables in python. You can set the rules for the 
variables. This can make your python project become more safer and easier to configure variables.

2. Install
-------------
Python3: pip3 install varplus

3. Useage
-------------
<pre>
<code>
from varplus import varbase as vb
vb.setVariable(name="test", value="Hello World!", rule={'noNone' : True}) #You can use noNone, variableType, isConst in rules
print(vb.getValue("test"))
vb.modifyValue("test", None) #You will get error, because your new data will be None
print(vb.isDeclared("test")) #It will print True
vb.clearVariable("test") #clear the variable test
print(vb.isDeclared("test")) #It will print False

vb.setVariable(name="test_2", value=1, rule={'noNone' : False, 'variableType' : 'int',  'isConst' : False})
print(vb.getValue("test_2")) #It will print 1
print(vb.isDeclared("test_2")) #It will print True
vb.modifyValue("test_2", "Hello World!") #You will get error, because test_2 variable data type is int not a string
vb.clearVariable("test_2")

vb.setVariable(name="test_3", value="It is const!", rule={'isConst' : True}) #this variable is const, you can't change data
print(vb.getValue("test_3")) #It will print It is const!
vb.modifyValue("test_3", "change!") #You will get error because test_3 is const, you can't change the data
</code>
</pre>

4. License
-------------

MIT License