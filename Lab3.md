Функція add2(x, y), яка повертає суму двох чисел.
add <- function(x, y) {
  x+y
}

add2(3,3)
[1] 6


Функція above(x, n), яка приймає вектор та число n, та повертає всі
елементі вектору, які більше n. По замовчуванню n = 10.

above <- function(x, n = 10) {
  x[x>n]
}

vektor <- c(1:15)
above(vektor)
above(vektor, 5)

[1] 11 12 13 14 15
 [1]  6  7  8  9 10 11 12 13 14 15
 
 
 Функція my_ifelse(x, exp, n), яка приймає вектор x, порівнює всі його
елементи за допомогою exp з n, та повертає елементи вектору, які
відповідають умові expression. Наприклад, my_ifelse(x, “>”, 0) повертає всі
елементи x, які більші 0. Exp може дорівнювати “<”, “>”, “<=”, “>=”, “==”.
Якщо exp не співпадає ні з одним з цих виразів, повертається вектор x.



my_ifelse <- function(x, exp, n) {
  if(exp == "<") {
    x[x < n]
  } else if(exp == ">") {
    x[x > n]
  } else if(exp == "<=") {
    x[x <= n]
  } else if(exp == ">=") {
    x[x >= n]
  } else if(exp == "==") {
    x[x == n]
  } else {
    x
  }
}

vektor2 <- c(1:15)
my_ifelse(vektor2, ">=", 10)
[1] 10 11 12 13 14 15

 Функція columnmean(x, removeNA), яка розраховує середнє значення
(mean) по кожному стовпцю матриці, або data frame. Логічний параметр
removeNA вказує, чи видаляти NA значення. По замовчуванню він
дорівнює TRUE.

columnmean <- function(x, removeNA = TRUE) {
  n <- ncol(x)
  if(removeNA == TRUE) {
    mean(x[ ,n], na.rm=TRUE)
  } else {
    mean(x[ ,n])
  }
}
 
 
 data <- data.frame(x = 1:15, y = c(1, 5, NA, 12, 0,0,0,0,0,0, NA, 67, 13, 14, 15))
columnmean(data)

[1] 9.769231
