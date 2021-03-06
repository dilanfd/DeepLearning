Author: Dilan Fernando

Email: dilan.fd@gmail.com

### Coding tips and tricks in Machine Learning and Deep Learning.

### This is a growing list...
    
If you have any tips and tricks to share send me a pull request. I will add it 
to the list and give you the credit.
	
	
1.	Avoid for loop and vectorize your code as much as you can.
	With a bit of Linear algebra most for loops in ML/DL can be
	vectorized.
	- Example:
		... TODO: Write example

2. Avoid 1D `numpy.arrays`. If you are dealing with a row vector explicitely
   make the dimension match that of the desired vector. Arrays of type 
   `(n,)` are bad for vectorization and will give unexpected errors and nasty
   bugs.
   - Example (Suppose you're looking for a 1 x 3 row vector):
	   
	   ```python
       a = np.array([1,2,3])
	   a.shape = (1, 3)
	   ```
	   
3. Use `assert` statements to insist `type` and `shape` etc. `assert` has
   constant time complexity and so it is cheap. Use it.
   - Example.
	 ```python
	 assert (isinstance(num, float))
	 
	 assert matrix.shape == (m , n)
	 ```

3. Use python broadcasting to your advantage.
   - Example:
	 ...

4. Use boolean masking whenever possible.
   - Example:
	 suppose you have a `p = np.array([0.34, 0.56, 0.99])` and 
	 you want to set `p = 1` when `value > 0.5` and `0` otherwise
	 you can do:
	 ```python
	 p = (p > 0.5)
	 ```
 
5. When using `numpy.sum` use the `axis=1` sums over the rows.
	`axis=0` sums over the columns. 
	
6. When using `numpy.sum` use the `keepdims=True` to keep the
   desired dimensions after the summation.
 
7. Use `numpy.multiply` for elementwise multiplication of matrices
   or vectors.

8. Use `numpy.squeeze()` to turn `[[15]]` into `15` after a vectorized
   computation.
   
   
