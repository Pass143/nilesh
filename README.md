# nilesh

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

    
