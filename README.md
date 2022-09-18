# Linear Algebra Tasks
### Linear algebra tasks which I have done during course of TFUG Azerbaijan
---
### Task 1 : Write a function which requires a matrix with arbitrary size and checks existence of being an orthogonal matrix made by elements of original matrix.
Input :
![ortho_1](https://user-images.githubusercontent.com/113797630/190878525-73a1086d-76a1-41e5-aaac-83d721c89f1e.png)
Output : 
![ortho_out](https://user-images.githubusercontent.com/113797630/190878568-5222cf24-f04c-4fc7-9d86-1f4af7a462e9.png)
---
![check_ortho_1](https://user-images.githubusercontent.com/113797630/190877626-abb0d35c-4ad6-4196-8bda-55c83b1b8ba7.png)

As seen in picture above, my function accepts array as argument and works on it under the name of **matrix** as it is called in this form in Linear Algebra. Then, in first step, size of matrix is changed from given shape to one row and number of elements (_matrix.size_) columns. In second step, it is changed to vector for being used in next processes.

So, what is the purpose of using **for** loop? I gave period of 100(_this number is chosen optionally, without any logic. You can use any number instead of it. I thought that more than 100 tries is nothing more than waste of time_) to generate different(_random_) matrices with the size of 2x2 from given(original) matrix elements. To talk about **if** and **else** conditions and the function(_is_ortho_) which **if** condition contains, we should look below :

![check_ortho_2](https://user-images.githubusercontent.com/113797630/190877842-3cfaaa1b-3340-478f-9c19-96e68332ee6f.png)

Function **is_ortho** firstly finds out inverse and transpose of the generated function(_it is repeated for each generation out of 100 periods_). As a last step, inside of **if** and **else** conditions, equality of those values(_inverse_ and _transpose_) is checked and is returned as result to the first function. So, if any orthogonal matrix exists, that will be returned with __'Yes'__ printing.

---
### Task  2 : Write a function which accepts a matrix as input with any size (3x3 or more) and should check existence of symmetric matrix of a matrix which has been made using elements of original matrix with the size of 3x3. Then it should return that symmetric matrix as final result
---
![sym_1](https://user-images.githubusercontent.com/113797630/190878613-30e11ae2-3bce-45bc-a751-c321ff3a2267.png)

Function **checking_having_symmetric** starts with condition of being in the shapes(_rows and columns_) of 3 or more. Following steps are the same as I written about in first task, the only difference is generating 3x3 matrices instead of 2x2. Let's continue with the most important part of progress, checking symmetry.

![sym_2](https://user-images.githubusercontent.com/113797630/190878870-ebf04074-f401-4454-8041-d9f05ece03c8.png)

To understand those steps, first we need to learn structure of symmetric matrix. So, let's look at it with the perspective of mathematics.

![sym_mat](https://user-images.githubusercontent.com/113797630/190878937-6a30ad7e-f021-4c4a-8c97-e4c55b8305eb.png)

As show above, diagonal elements don't have any impact of symmetry. However, rest of the elements are playing managable role. Each of them (except diagonal elements) should be equal to the element with replaced indices(_row and column number_). In other words, if a matrix is equal to its transpose, then it's called as **symmetric matrix**.

Go back to the code, working principle of those nested loops are the same as I expressed with being equal to the elements with replaced indices of themselves. So, total program checks 100 tries again, and figures out all symmetric matrices by returning them.
