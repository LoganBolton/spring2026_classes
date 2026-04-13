# Assignment 5 - Logan Bolton

**1. What are the building blocks that the authors proposed to generate arbitrary activation functions?**

They built activation functions out of small core units. Each core unit has two unary functions and one binary function. They try different combinations of unary functions combined with binary functions to find new activation functions. 

**2. What is probably the reason that activation functions that contain divisions perform poorly?**

When the denominator is close to zero, the activation output becomes very large. This can cause training instability.

**3. Does making β in the swish activation function trainable provides any advantage? How did the authors prove that?**

Yes, making β trainable can help. They directly compared Swish with trainable β against Swish-1 with fixed β = 1 in their experiments across different models and datasets. They also looked at the learned β values and found that they spread across different values instead of all staying at 1. This suggests that the model was using the extra flexibility.