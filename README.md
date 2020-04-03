# deep-chicken-saviour :shield: :chicken:

<img src = "images/adversarial_attack.png" width = "100%">

## Fast Gradient Sign Method :chart_with_upwards_trend:

* `sign(data_gradients)` gives the element wise signs of the data gradient
* `epsilon` defines the "strength" of the perturbation of the image

In a nutshell, instead of **optimizing the model to reduce the loss**, we're **un-optimizing the input image to maximise loss**.

* This works primarily because of the piecewise linear nature of deep neural networks. For example, look at ReLU or at maxout functions, they're all piecewise linear. Even a carefully tuned sigmoid has an approximate linear nature when taken piecewise.

* With varying values of epsilon, we will see an approximately linear relationship between "confidence" and epsilon.
