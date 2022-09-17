# Linear Algebra Tasks
Linear algebra tasks which I have done during course of TFUG Azerbaijan

First task: Write a function which requires a matrix with arbitrary size and checks existence of being an orthogonal matrix made by elements of original matrix.

![check_ortho_1](https://user-images.githubusercontent.com/113797630/190877626-abb0d35c-4ad6-4196-8bda-55c83b1b8ba7.png)

As seen in picture above, my function accepts array as argument and works on it under the name of **matrix** as it is called in this form in Linear Algebra. Then, in first step, size of matrix is changed from given shape to one row and number of elements (__matrix.size__) columns. In second step, it is changed to vector for being used in next processes.

So, what is the purpose of using **for** loop? I gave period of 100(__this number is chosen optionally, without any logic. You can use any number instead of it. I thought that more than 100 tries is nothing more than waste of time__) to generate different(__random) matrices with the size of 2x2 from given(original) matrix elements. To talk about **if** and **else** conditions and the function which **if** condition contains, we should look below :

![check_ortho_2](https://user-images.githubusercontent.com/113797630/190877842-3cfaaa1b-3340-478f-9c19-96e68332ee6f.png)

Our **is_ortho** function firstly finds out inverse and transpose of the generated function(__it is repeated for each generation out of 100 period__). As a last step, inside of **if** and **else** conditions, equality of those values(__inverse__ and __transpose__) is checked and is returned as result to the first function. So, if any orthogonal matrix exists, that will be returned with 'Yes' printing.
