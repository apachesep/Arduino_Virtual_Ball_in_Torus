# Arduino Virtual Ball in Torus

This small Arduino construction reproduces the machanics of a ball kept inside a torus. By moving the Arduino board itself accross the 6 dimansions, the ball circulates inside.

The behavior is calculated realtime by the processor, based on standard mechanics equations, using moment of inertia.

All calculations are based on Euler angles, in the canonical (first) approach based on the ZXZ angles: &#x03c8 (psi), &#x03b8 (theta) then &#x03c6 (phi). This picture from [Berkeley University](https://rotations.berkeley.edu/the-euler-angle-parameterization/) explains the used notation.

![Euler angles](./euler-angles.png)

Assuming a fixed board, the only of the gravity force is:

![Moment from gravity force](./equ-gravity.svg)

Then as the board is actually a non galilean referencial, moment of virtual forces appply. The 3 forces are the Euler force, the Coriolis force and the centrifugal force. The 3 forces are explained [here](https://en.wikipedia.org/wiki/Coriolis_force).

![Non Galilean virtual forces](./non_galilean_virtual_forces.svg)

Each moment is equal to:

So the final equation is:

I have calculated all the equations myself, so if you find any error, please contact me!