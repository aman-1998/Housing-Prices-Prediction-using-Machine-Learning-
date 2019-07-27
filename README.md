Housing Prices Prediction- using Machine-Learning:-


Algorithm used:

Housing Prices Prediction though Single Variate Linear Regression using "Gradient Descent" Algorithm

Mathematical Formulation:

y = mx + c

 where m = slope (or, weight = W)
       c = intercept (or, bias = b)
       x = feature
       y = predicted value of target_var
e = mean {(y - t)^2}

 where y = y(p){mpg predicted} 
       t = y(d) {mpg from dataset given i.e., target value} 
Note: The grapah of the error function is convex. So, we can apply Gradient Descent Algo to get the minimum error

Gradient Descent Algorithm (Geometric Intuition):
It is an iterative optimization algo with update eqn: x(i) = x(i-1) - r* {{∂f(x)/∂x}| @ x=x(i-1)}

Now in Linear Regression, since we've to to minimize slope and intercept to minimize the error (or cost, or loss) function; we use:

m = m - {r*(∂(e)/∂(m))

 where ∂(e)/∂(m)= ∂(mean((y-t)^2))/∂(m) 
                 = ∂(mean(mx+c-t)^2))/∂(m) 
                 = 2*mean(mx+c-t)* {∂(mx)/∂(m) + ∂(c-t)/∂(m)} 
                 = 2*mean(mx+c-t)* {x + 0} 
                 = 2*mean(mx+c-t)* (x) 
c = c -{r*(∂(e)/∂(c))}

 where ∂(e)/∂(c) = ∂(mean((y-t)^2))/∂(c) 
                 = ∂(mean(mx+c-t)^2))/∂(c) 
                 = 2*mean(mx+c-t)* {∂(mx)/∂(c)+∂(c)/∂(c)-∂(t)/∂(c)} 
                 = 2*mean(mx+c-t)* {0 + 1 -0} 
                 = 2*mean(mx+c-t)
e = mean {(y-t)^2

     if y = t, then e(min) = 0
     if y = 0, then e(max) = mean(t^2)
poe (i.e., %_of_error) = {current error / {(e(max))^2} } * 100

         = {current error / mean(t^2)} * 100 

         = {current error / mean(target^2)} * 100 

      [Note: this formual is for prediction, not classification]
poa (i.e., %_of_accuracy) = 100 - poe
