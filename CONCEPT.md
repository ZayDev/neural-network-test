### A simple NN

# Images with: http://asciiflow.com

        +b0,0
     +-->N1+--+
  *w0,0      *w1,0
     |        |
I ------>N2+----->O
     |        |  +b1
     |        |
     +-->N3+--+



## Acronyms
N?   -> Neuron and it's corresponding value
w?,? -> Weight of my neuron connection on (layer,number)
b?,? -> the bias of my N?
I    -> Input neuron/ value
O    -> Output neuron/ value

# Sigmoid activation function // https://de.wikipedia.org/wiki/Sigmoidfunktion
S(a) = 1/(1+e^a)


## MATH

N1 = S(I*w0,0) + b0,0

O  = S(N1*w1,0 + N2*w1,1 + N3*w1,2) + b1
