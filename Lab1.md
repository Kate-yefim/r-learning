1. Створити змінні базових (atomic) типів. Базові типи: character, numeric,
integer, complex, logical.

num <- numeric()

char <- character()

compl <- complex()

int <- integer()

log <- logical()

2. Створити вектори, які: містить послідовність з 5 до 75; містить числа 3.14,
2.71, 0, 13; 100 значень TRUE.

first_vec <- 5:75

second_vec <- c(3.14, 2.71, 0, 13)

third_vec <- !logical(100)

3. Створити наступну матрицю за допомогою matrix, та за допомогою cbind
або rbind
0.5 1.3 3.5
3.9 131 2.8
0 2.2 4.6
2 7 5.1

My_matrix <- matrix(data = c(0.5, 1.3, 3.5, 3.9, 131, 2.8, 0, 2.2, 4.6, 2, 7, 5.1), ncol = 3, byrow = TRUE)

My_matrix

Same_matrix <- rbind(c(0.5, 1.3, 3.5), c(3.9, 131, 2.8), c(0, 2.2, 4.6), c(2, 7, 5.1))

Same_matrix


4. Створити довільний список (list), в який включити всі базові типи.

new_list <- list(num, char, compl, int, log)

5. Створити фактор з трьома рівнями «baby», «child», «adult».

age <- factor(c(), levels = c("baby", "child", "adult"))

age

6. Знайти індекс першого значення NA в векторі 1, 2, 3, 4, NA, 6, 7, NA, 9, NA, 11. Знайти кількість значень NA.

weird_vector <- c(1, 2, 3, 4, NA, 6, 7, NA, 9, NA, 11)

index <- 1:length(weird_vector)

indexes_NA <- index[is.na(weird_vector)] ##indexes NA

indexes_NA[1] ##have no idea how to do it without indexes (help)

table(is.na(weird_vector))["TRUE"] ##how many NA

7. Створити довільний data frame та вивести в консоль.

My_data <- data.frame(animals = c("bear", "otter", "cat", "bat", "elephant"), is_cool = c(T, T, T, T, T),
                      is_dangerous = c(F, F, F, T, F), height_in_meters = c(3, 0.5, 0.3, 0.1, 5))

My_data

8. Змінити імена стовпців цього data frame.

names(My_data) <- c("Animal species", "Is animal cool", "Is animal dangerous", "Height of animal in meters")

x`My_data
