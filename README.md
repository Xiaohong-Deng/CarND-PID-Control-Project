# CarND-Controls-PID
Self-Driving Car Engineer Nanodegree Program

---

## Effect of P, I, D components

P component is used to adjust steer angle based on cross track errors. With P component alone, as error goes down P becomes smaller but the angle tends to reflect that slower. The consequence is the vehicle oscillates around the path.

D component is used to compensate that effect. It is the difference between current cross track error and the cross track error from the last time step. So if in the last time step error is greatly reduced, we add a much smaller steer angle even if the error is still positive.

I component is used to compensate the drift bias. If the vehicle adds a certain amount of error to your control angle, you accumulate the actual cross track errors you observe over time, use that to increase or decrease the control angle.

## Hyperparameters
I plugged in PID coefficients from the lectures and it worked. Honestly I don't know how to use the simulator to run twiddle and save the best parameters, then restart the simulation with the optimal parameters. Do I need to call `onMessage` twice in a row? How does that work?

As for SGD, I don't know that, either. Can you give me some orientation? 
