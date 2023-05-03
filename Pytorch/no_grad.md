Context-manager that disabled gradient calculation.

can be applied to functions with @ decorator
```
x = torch.tensor([1.], requires_grad=True)
with torch.no_grad():
    y = x * 2
y.requires_grad
@torch.no_grad()
def doubler(x):
    return x * 2
z = doubler(x)
z.requires_grad
```


Use of Torch.no_grad():

- To perform inference without Gradient Calculation.

- To make sure there's no leak test data into the model.

It's generally used to perform Validation. Reason in this case one can use validation batch of large size.


__Resources__
- https://pytorch.org/docs/stable/generated/torch.no_grad.html
- https://www.tutorialspoint.com/what-does-with-torch-no-grad-do-in-pytorch#:~:text=The%20use%20of%20%22with%20torch,detached%20from%20the%20current%20graph.
- https://datascience.stackexchange.com/questions/32651/what-is-the-use-of-torch-no-grad-in-pytorch
