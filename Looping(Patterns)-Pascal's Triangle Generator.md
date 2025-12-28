# 🔺 Looping(Patterns)-Pascal's Triangle Generator in Python

This project demonstrates a simple Python program to generate **Pascal’s Triangle**, where the number of rows is provided by the user.

---

## 🎯 Aim

To write a Python program that generates **Pascal's Triangle** using numbers. The number of rows is accepted from the user.

---

## 🧠 Algorithm

1. Start the program.
2. Input the number of rows from the user.
3. Loop from 0 to the number of rows.
4. For each row:
   - Print appropriate spaces to shape the triangle.
   - Compute values using the formula:  
     \[
     C(n, k) = \frac{n!}{k!(n-k)!}
     \]
5. Print all rows of Pascal’s Triangle.
6. End the program.

---

## 🧪 Program
```
def pascal(row):
    triangle=[]
    for a in range(row):
        cur_row=[1]*(a+1)
        if a>1:
            prev_row=triangle[a-1]
            for i in range(1,a):
                cur_row[i]=prev_row[i-1]+prev_row[i]
        triangle.append(cur_row)
    for b in triangle:
        print(" ".join(map(str,b)))
row=int(input())
pascal(row)
```
## Sample Output
<img width="496" height="480" alt="image" src="https://github.com/user-attachments/assets/a20990a2-32fe-41fc-9ce7-ad47f80b78c8" />

## Result

