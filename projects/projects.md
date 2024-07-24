# Projects

These are just projects that I use to keep myself occupied :)

## MatrixKit and NeuralKit

`MatrixKit` and `NeuralKit` are two libraries I developed in tandem with the goal of creating a simple machine learning
library for Swift. Apple has plenty of (more functional) machine learning libraries you can use right from Xcode,
but in my opinion they were not beginner friendly and did not have very intuitive ways to actually craft and train
your own neural network. So, I created my own! Also, I figured that writing a machine learning library from scratch would 
teach me a *lot* more about machine learning than just using other libraries or reading about it. So, `NeuralKit`
does not use *any* external libraries other than `MatrixKit`, which I also wrote. 

`MatrixKit` is an abstract linear algebra library. By "abstract", I mean that you've got this cool `Matrix` type which
has elements that can be entries in any arbitrary ring! If entries are in a field, this is automatically detected and 
you can compute matrix inverses in the like.

There was an interesting problem I had about computing row-echelon form. When the matrix only has entries in a 
ring and we can't do division, we ought to be able to do REF! The issue I run into is that without being able to divide
to "re-normalize" things, entries often grow out of control and the matrix blows up.

## rusty_crypto

## algebra_kit and matrix_kit

## BigNumber and sylvan_number

