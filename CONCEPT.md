# Concepts for a simple NN

Images with: Monodraw for OS X


```                                         
                   +b0,0                    
                  ┌────┐                    
       ┌─────────▶│ N1 │──────────┐         
       │          └────┘          │         
    *w0,0-0                    *w1,0-0      
       │                          │         
       │           +b0,1          │    +b1,0
┏━━┓   │          ┌────┐          │   ┏━━━┓ 
┃In┃───┼─────────▶│ N2 │──────────┼──▶┃Out┃ 
┗━━┛   │  *w0,0-1 └────┘ *w1,1-0  │   ┗━━━┛ 
       │                          │         
       │                          │         
    *w0,0-2        +b0,2       *w1,2-0      
       │          ┌────┐          │         
       └─────────▶│ N3 │──────────┘         
                  └────┘                    
```                                         


### Acronyms

| Acr.   | Meaning |
| ------ | ------- |
| N? | Neuron *?* |
| w?,a-b | The weight of the connection between neuron *a-b* ending at layer *?* |
| b?,a | The bias of the N*a* on layer *?* | 
| I | Input neuron |
| O | Output neuron |


## Math I

Every neuron calculates it's value by summing over every input (multiplied by it's corresponding weigth) then adding the bias to the result, just to apply in the last step the activation function to the whole equation.

`A( ∑( N_n * w_?,n-? ) + b_?,? )`

In this example we'll be using the sigmoid activation function. For a closer look see: https://de.wikipedia.org/wiki/Sigmoidfunktion

`S(a) = 1/(1+e^a)`


That means for our network we've the formulas:

`N1 = S(I*w0,0-0 + b0,0)`

`O  = S(N1*w1,0-0 + N2*w1,1-0 + N3*w1,2-0 + b1,0)`

...and so on.


**Try to write an implementation till to this point!**
> It doesn't need to be big, just a simple python script.
