# ENGR 102 Lab Assignment #1b
## Activity #4: Assignment: Writing your own Programs (Individual)

### Program 1:
The purpose of this program is to familiarize you with some basic Engineering equations, as well as to have practice writing a simple Python program that performs calculations.

In the new Zachry Engineering Quad, you will find 50 different equations relevant to various aspects of Engineering. The equations referenced below appear among these equations. You may wish to go find where each of them appears in the E-quad!

Write a program that outputs each of the following, on subsequent lines. We will ignore units in these equations. You will likely need to look up some of the formulas for some of these online (it's fine to do so – that is part of the task!). You may discuss where to find information about these equations with other students, but you should actually read the details and write the computations yourself. The actual output should be the result of the calculation. Your code should show the full calculation. For instance, if the task is to print the area of a square with side length 5, you would want to have a line such as:

```
print(5*5)
```

And not the line:

```
print(25)
```

You should have 10 lines of output, giving each of the following. If you do not have a result for one of these, print an empty line, or the text "no answer" in that line.

a) Your name, UIN, and section number of ENGR 102 that you are enrolled in

b) A sentence giving some interesting fact about yourself

c) The voltage across a conductor with resistance 20 and a current of 5.
   - Ohm's Law states that the current through a conductor between two points is directly proportional to the voltage across the two points.

d) The kinetic energy of an object with mass 100 and velocity 21
   - The Kinetic Energy of an object is the energy that it possesses due to its motion. The standard unit of kinetic energy is the joule.

e) The Reynolds number for a fluid with velocity 100 and kinematic viscosity 1.2, with characteristic linear dimension 2.5.
   - The Reynolds Number is an important dimensionless quantity in fluid mechanics that is used predict flow patterns in different fluid flow situations. It is the ratio of inertial forces to viscous forces.

f) The energy radiated per unit surface area (across all wavelengths) for a black body with temperature 2200. Use 5.67 x 10^-8 for the Stefan-Boltzmann constant.
   - The Stefan-Boltzmann Law describes the power radiated from a black body in terms of its temperature. Specifically, the total energy radiated per unit surface area of a black body across all wavelengths per unit time is proportional to the fourth power of the black body's thermodynamic temperature.

g) The production of a well after 20 days, if it had an initial production rate of 100, an initial decline rate of 2/day, and a hyperbolic constant of 0.8
   - Arps equation is a mathematical model to forecast future production rates of oil and gas wells.

h) The average length of an M/M/1 queue with an arrival rate of 20 and a service rate of 35.
   - An M/M/1 Queue represents the queue length in a system having a single server, where arrivals are determined by a Poisson process and job service times have an exponential distribution. The model is the most elementary of queueing models.

i) The shear stress when a normal stress of 20 is applied to a material with cohesion 2 and angle of internal friction 35 degrees
   - The Mohr-Coulomb Failure Criterion represents the linear envelope that is obtained from a plot of the shear strength of a material versus the applied normal stress. More generally, the Mohr–Coulomb theory is a mathematical model that describes the response of brittle materials, like concrete or rubble piles, to shear stress as well as normal stress. Most of the classical engineering materials somehow follow this rule in at least a portion of their shear failure envelope.

j) The scattering angle for maximum interference for light of wavelength 7.5 x 10^-7 hitting a crystalline lattice with planes separated by a distance 1 x 10^-6.
   - Bragg's Law is a relationship describing the angles for coherent and incoherent scattering from a crystal lattice. Specifically, it describes the condition for maximum constructive interference.

### Program 2:
The purpose of this program is to introduce how limits, which you will see in calculus and work with analytically, can be calculated numerically. This also exercises creating computational Python programs.

You are to write a program that produces several evaluations. Later in the course, we will see other ways of doing this more efficiently, but for now, you should perform these evaluations by simply creating a sequence of print statements that output the desired numbers.

Certain functions might be difficult to evaluate at particular values, where infinity or division by 0 are involved, but could be understood by evaluating them at a number of values that approach 0 or approach infinity. You are going to investigate three of these.

Important: You are to think about each of these briefly, and guess what they will come to, before writing your code! There is no penalty for wrong guesses.

You should write a program that, for each of these functions:

a) First prints out a line of text at the beginning, stating what is being shown in the following lines.
   - e.g. printing "This shows the evaluation of 5*x/(x-2) evaluated close to x=1"

b) Next, prints out a line of text saying what you are guessing the final value you calculate will come to. There is not a wrong answer here as long as you make a guess – the point is to get you to think about the value first, and then see whether your guess was close or not.
   - e.g. printing "my guess is -3.0"

c) Finally, prints out a sequence of 7 numbers, representing evaluating the function at 8 different values.
   - e.g. evaluating 5*x/(x-2) at 1.1, 1.01, 1.001, … 1.00000001 and outputting results would give:

```
-6.111111111111112
-5.101010101010101
-5.010010010010008
-5.001000100010001
-5.0001000010000105
-5.00001000001
-5.0000010000001005
-5.0000001
```

   - Notice that the evaluation gets closer and closer to -5, in this case.

#### Function 1: 
The function f(x) = sin(x)/x is not defined at the value 0, since sin(0) is 0, and thus it would be evaluating 0/0.

a) You are to show calculations for the values of f(x) for values of x ranging from 1 to 10^-7.
b) You should show the evaluation by successive evaluations of 1/10 of the previous value. That is, first show the value for sin(1)/1, then sin(0.1)/0.1, etc.

#### Function 2: 
The function g(x) = (1-cos(x))/x^2 is not defined at the value 0, since cos(0) is 1, and thus it would be evaluating to 0/0.

a) You are to show calculations for the values of g(x) for values of x ranging from 1 to 10^-7.
b) You should show the evaluation by successive evaluations of 1/10 of the previous value.

#### Function 3: 
The function h(x) = (1+1/x)^x cannot be directly evaluated at infinity. Because, well, it's infinity.

a) You are to show calculations for the values of h(x) for values of x ranging from 1 to 10^7.
b) You should show the evaluation by successive evaluations of 10 times the previous value. i.e. evaluate at values of 1, 10, 100, etc.
