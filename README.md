# clc
clear all
disp('------Y BUS Formation------');
x=input ('Enter the number of nodes: ');
for i=1:1:x
 for j=1:1:x
 if(i==j)
 a(i,j)= input(strcat('Enter the value of 
admittance Y',int2str(i),int2str(0),':')); 
 else
 a(i,j)= input(strcat('Enter the value of 
admittance Y',int2str(i),int2str(j),':')); 
 end
 end
end
b=a; y=0;
for i=1:1:x
 for j=1:1:xif i==j

 for k=1:1:x

 y=y+b(i,k); 

 end

 a(i,j)=y;

 y=0;

 else

 a(i,j)= -b(i,j);

 end 

 end

end

b;

YBUS=a;
INPUT: 

Enter no. of buses: 4 

Y10= -1 Y12= -2.5 Y13= -5 Y14= -0 Y21= -2.5 Y22= -1.25 Y23= -5 

Y24= -0 Y31= -5 Y32= -5 Y30= 0 Y34= -12.5 Y41= 0 Y42= 0 Y43= -12.5 Y40= 0

# Program for Intermediate Value Theorem

import matplotlib.pyplot as plt

import numpy as np

#Function Definition

def f(x):

     y=x*x+5*x+6

     return y

# Main Program

# Input Section

a=float(input('Enter initial value of a:'))

b=float(input('Enter initial value of b:'))

# Plotting function

x=[]; y=[]

for v in range(0, 11, 1):

      x.append(a+(b-a)*v/10)

      y.append(f(a+(b-a)*v/10))

plt.plot(x, y)

plt.grid()

plt.show()

# Process and output section

if f(a)*f(b)<0:

     print('root lies in the interval [a, b]=',a,b)

elif f(a)*f(b)==0:

     print('any one initial value may the root')

else:

     print('No lies in the interval [a, b]=',a,b)

    
