# PID Control Project

#### Describe the effect each of the P, I, D components had in your implementation.

The P component is the main driving force of the correction of steering direction. With P component only, the car would oscillate around the desired driving direction. When going into a turn the oscillation will amplify and drives the car out of the driveway. A larger P component performs better at sharp turns since it will react to the change of the cross track error. 

The D component can add a little damping effect to the oscillation caused by P component. With proper D component, the car will drive more smoothly. But with higher value of the P component, D component needs to increase as well to provide effective damping. With P and D components only, the car can steer through the map already. 

The I component is added to correct for system bias. Since the car can drive through the track with no problem with I=0. I think the system bias is small if any. But I component, in theory should correct for the accumulation of small bias signal. 

### Describe how the final hyperparameters were chosen. 

The hyper parameters were chosen by hand tuning. The P component was decided, mainly to guarantee that the can is capable to turn through the sharper turns in the map. The D parameter was chosen to minimize the oscillation in the steering. The I parameter is really small, it didn't make much difference. So I kept it at a really low but not ignorable size (0.0001).