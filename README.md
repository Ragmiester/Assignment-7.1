values=[3, 5, 7, 2, 8, 10, 11, 65, 72, 81, 99, 100, 150]
interval=3
import numpy as nm
def movavg(x,y):
    c=nm.cumsum(nm.insert(x,0,0)) #list of cummilative starting with 0
    d=nm.asarray((c[y:] - c[:-y])/y)# numerator is the required cummilation as it takes the difference between the 
                                    #last y (interval) and the first y (interval) demonator takes the average
    return d, type(d)
print("moving average: ", movavg(values,interval))

# Assignment-7.1
Assignment 7.1
