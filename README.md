# Overview
I am an [M.S. student](https://www.cs.cornell.edu/ms) at Cornell University where I am advised by [Robert Kleinberg](https://www.cs.cornell.edu/~rdk/). 

I completed my undergrad at Cornell in Math and CS. I am interested in networks,
graph algorithms, randomized algorithms, and cryptography (and other stuff too!). Here is a 
[link to my resume.](files/Sylvan%20Martin%20Resume.pdf)

Outside of schoolwork, I am a [rock climbing](climbing/CLIMBING.md), caving, and 
[tree climbing](climbing/CLIMBING.md/#tree-climbing) instructor for Cornell Outdoor Education! I also guided [Outdoor Odyssey](https://scl.cornell.edu/coe/odyssey)
trips for incoming freshmen.

Email: `sylvan.martin@gmail.com`

**Contents**
1. [Overview](#overview)
2. [Publications](#publications)
3. [Projects](#projects)
4. [Writeups](#tutorials-and-writeups)
5. [Climbing](climbing/CLIMBING.md)

# Publications

- **Universal Connection Schedules for Reconfigurable Networking.** To appear at *SODA 2026*. Shaleen Baral, Robert Kleinberg, **Sylvan Martin**, Henry Rogers, Tegan Wilson, and Ruogu Zhang.

# Projects
I love making fun projects, here are some of the more relevant/recent ones over the years. Below, you'll also 
find 

## [ml_kit](https://github.com/SylvanM/ml_kit)

There is a dearth of machine learning libraries for Rust, since it's such a new language. But, I think that's a missed 
opportunity! Rust is great! So, for my CS practicum course at Cornell, my group (me, Owen Wetherbee, and Ethan Ma)
created a machine learning library written in pure Rust, containing tools to do deep learning (neural networks, 
convolutional neural networks, and the training thereof) and singular value decomposition along with its 
applications (PCA, image compression, regression/planes of best fit). [Here is our writeup](https://github.com/SylvanM/ml_kit/blob/main/writeups/final/final_report.pdf) that we submitted
for the class.


## [Hemlock](https://github.com/SylvanM/hemlock_lib)

This is a Rust application that uses Shamir Secret Sharing to securely and redundantly do cloud storage when there is 
a lack of trust among parties. The intended audience would be a company or large organization with sensitive information
that doesn't need to be regularly accessed (think a hospital's patient data, or the addresses of clients). If there 
is a single password or key that can access this information, that makes for a single point of failure. This splits 
that responsibility among multiple individuals, so that in order to access the data, some fraction of those individuals
must agree. The Hemlock app is my implementation of this, and makes calls to a cloud database to store the secrets, users,
and keys. The linked project is just a rust library, but I also began working on a GUI, found [here](https://github.com/SylvanM/Hemlock). 

### MatrixKit and NeuralKit (Swift)

`MatrixKit` and `NeuralKit` are two libraries I developed in tandem with the goal of creating a simple machine learning
library for Swift. Apple has plenty of (more functional) machine learning libraries you can use right from Xcode,
but in my opinion they were not beginner friendly and did not have very intuitive ways to actually craft and train
your own neural network. So, I created my own! Also, I figured that writing a machine learning library from scratch would 
teach me a *lot* more about machine learning than just using other libraries or reading about it. So, `NeuralKit`
does not use *any* external libraries other than `MatrixKit`, which I also wrote. 

`MatrixKit` is an abstract linear algebra library. By abstract, I mean that you've got this cool `Matrix` type which
has elements that can be entries in any arbitrary ring! If entries are in a field, this is detected and 
you can compute matrix inverses and the like.

There was an interesting problem I had about computing row-echelon form. When the matrix only has entries in a 
ring and we can't do division, we ought to be able to do REF! The issue I run into is that without being able to divide
to "re-normalize" things, entries often grow out of control and the matrix blows up.

 - [ml_kit](https://github.com/SylvanM/ml_kit): A machine learning library for Rust, in collaboration with Owen Wetherbee and Ethan Ma
 - [rusty_crypto](https://github.com/SylvanM/rusty_crypto): A post-quantum cryptographic suite written in Rust
 - [algebra_kit](https://github.com/SylvanM/algebra_kit): An abstract algebra library for Rust
 - [matrix_kit](https://github.com/SylvanM/matrix_kit): An abstract *linear* algebra library for Rust (sensing a pattern here?)
 - [Ocaml ECC](https://github.com/SylvanM/cs3110-sectool): Elliptic-Curve Diffie-Helman in OCaml
 - [BigNumber](https://github.com/SylvanM/BigNumber): A performance based big-integer library for Swift

There are many more but these are just some of my favorites.

# Tutorials and Writeups

As I'm working on new projects, there are certain problems I run into that I realize I will need to re-solve in later projects,
or that other people will run into as well. For a lot of these problems, there exists a good online tutorial already written. But,
for some topics, I could not find a (in my opinion) well-written tutorial online that actually answered the questions I had.
So, I'm writing tutorials and explainers for others and mainly for myself! If you see a typo feel free to let me know.

### Machine Learning

- [An explanation of Backpropogation](ml/notes.pdf) that I wrote up after a group meeting (for the [ml_kit](https://github.com/SylvanM/ml_kit) project) where we worked out the math behind backpropogation, because we couldn't really find a good, complete explanation elsewhere. 

### Cryptography

- [Learning With Errors](cryptography/lwe.pdf)

### Writeups I want to make

- Calling (Asynchronous!) Rust Code from C and Swift
	- This one is [hard](https://www.reddit.com/r/rust/comments/w2tlzv/comment/igs8797/?utm_source=share&utm_medium=web3x&utm_name=web3xcss&utm_term=1&utm_content=share_button) because of how C and Swift manage their memory differently, and what variables you can 
	and can't pass into closures. I found a way to get it working for very simple cases (which I call a ["callback table"](https://github.com/SylvanM/Hemlock/blob/main/Hemlock/Utility/HL%20Core%20API/HLCore.swift)) but it won't work when multiple asynchronous calls are being 
	made at once. I'm still working on this, and when I figure it out I'll write something about it here!
- Implementing Big Number division
	- You might think this ought to be straightforward, but I found a lot of caveats that come up when actually trying to implement,
	say, Knuth's algorithm from TAoCP.

# [Rock Climbing](climbing/CLIMBING.md)
And [here](climbing/CLIMBING.md) is where you can see cool rock climbing stuff!
