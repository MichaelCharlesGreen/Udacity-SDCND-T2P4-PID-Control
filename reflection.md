#PID Project Reflection

### [PID Simulator Video](https://youtu.be/HkaQ6I8IuGk)

The final P, I, and D values are: 0.19, 0.001, and 3.1.

When running the program, enter them on the command line as following: ./pid 0.19 0.001 3.1

### Describe the effect each of the P, I, D components had in your implementation.

##### P Component
Produces an output proportional to the cross-track error (CTE).

##### I Component
Produces an output proportional to the integral of the CTE.

##### D Component
Produces an output proportional to the derivative of the CTE.

### Describe how the final hyperparameters were chosen.

All three coefficients, P, I, and D began at 0.

The P coefficient was tuned first by orders of magnitude to determine how the outcome was affected until the car made it to the left turn after the bridge at which point it failed to make the turn.

The D coefficient was then turned by orders of magnitude to mitigate oscillation and make it passed the left turn after the bridge.

Improvement could be seen earlier in the simulator (prior to the left turn after the bridge) as the D coefficient was tuned.

To improve performance (increase speed, increase boldness of steering correction, decrease steering correction oscillation or jitter), the P and D coefficients were altered in tandem, which consisted of increasing P and then increasing D in response to the jitter introduced.

Finally, the I component was tuned to correct what may have been a system bias which presents as an offset in the simulator, i.e., the car runs slightly off-center on the track.


