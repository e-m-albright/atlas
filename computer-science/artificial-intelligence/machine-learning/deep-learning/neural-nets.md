# Neural Nets

Activation functions may accidentally shrink weights to near 0, creating small gradients and slowing learning by a ton

derivative of W\*X with respect to W is just X, if anything in backprop is near 0 it goes to near 0... \(half understood note\)

Same problem occurs with functions like tanh, neurons become saturated to -1 or 1 and gradients will likewise be effectively 0.

### Xavier Initialization

Initialize weights to random gaussian numbers with stdev equal to 1 / fan\_in we maintain the right size of the weights for longer. This doesn't fully stabilize the system though and the weights will still fall out of balance.

IF you use something like ReLU's doesn't work. There are alternative styles of initialization to work better with ReLU's, but it's always the same typical problem of eventual shrink/blow up.

### Batch Normalization

This is dynamically responding to and stabilizing the size of the data.

The lack of these prevented deep layers in the initial history of neural nets \(5 layers work, 10 layers doesn't\)

Mean centered on 0, stdev of 1. Keeps things balanced around 1?

Layers added to "fix up" or balance each unit. Usually inserted after fully connected or convolutional layers and before non-linearity.

Often also adds in scaling up \(modifier\) and adding scalars \(offset\) to control how you want things to grow or shrink instead of letting it happen naturally.

Helps with gradient flow through the network, allows higher learning rates \(unclear of meaning?\), reduces dependence on initialization \(rebalance bad starts, self corrects\), and regularizes a little \(shrinks large weights, expands small ones I guess?\)

