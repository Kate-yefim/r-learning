1. Створить вектор v із 100 елементів командою v <- rnorm(100). Для цього
вектору виведіть: 10-й елемент; елементи з 10-го по 20-й включно; 10
елементів починаючи з 20-го; елементи більше 0.

v <- rnorm(100)
v

[1]  3.186676843  1.277891796  0.147297833 -1.528676688 -1.145375147  0.966548552  1.027344322 -0.276826026 -0.816543391

[10]  1.101015674  1.507267695  1.141646422  0.359046223  1.568174830  0.214405842 -1.192730397 -0.556929345  0.639961073
[19] -1.246820166  0.115414447 -0.836596227  0.087246437 -0.562627018  1.525166232 -0.141021332 -0.993416178  0.138658183
[28]  0.783060089 -1.041449388 -0.191626249 -0.084375996  0.271928546  0.104217946 -2.019598626  0.838444329 -1.277853543
[37]  0.520105161  0.366449255 -0.155168242 -2.106449012 -1.558981072 -0.567314694 -0.298830327  0.005144287 -1.505452013
[46]  0.077075053 -0.161588300 -0.655676712 -1.110574674 -0.402370872  1.148630494  1.752299898 -2.385499715  0.432396940
[55] -0.066108615  1.039180549  0.637075235 -0.423373253  1.063502938  0.265507310  1.066961326 -0.689446876  1.039989547
[64] -1.047264463 -2.708419912 -0.219571569 -0.915616776 -1.570245061 -1.455432232 -1.373951229 -0.079912504 -0.085755606
[73]  0.958572017 -0.895165859 -0.213713998 -0.863204772 -1.143944269  1.246700633  0.905354225 -0.594054894  1.666109162
[82] -1.052442586  0.358623021  0.740307691 -0.294155434  1.409810024 -1.601941275 -1.060639191 -0.585729963 -0.357171548
[91] -0.684658293  0.125895274  2.233172570 -0.143978212 -1.293724816 -2.076421517  0.595393165 -0.513841179  0.794973662
[100] -0.955285916

##10-й елемент

v[10]

[1] 1.101016

##елементи з 10-го по 20-й включно

v[10:20]

[1]  1.1010157  1.5072677  1.1416464  0.3590462  1.5681748  0.2144058 -1.1927304 -0.5569293  0.6399611 -1.2468202  0.1154144

##10 елементів починаючи з 20-го

v[(i<-20):(i+9)]

[1]  0.11541445 -0.83659623  0.08724644 -0.56262702  1.52516623 -0.14102133 -0.99341618  0.13865818  0.78306009 -1.04144939

##елементи більше 0

v[v>0]

[1] 3.186676843 1.277891796 0.147297833 0.966548552 1.027344322 1.101015674 1.507267695 1.141646422 0.359046223 1.568174830
[11] 0.214405842 0.639961073 0.115414447 0.087246437 1.525166232 0.138658183 0.783060089 0.271928546 0.104217946 0.838444329
[21] 0.520105161 0.366449255 0.005144287 0.077075053 1.148630494 1.752299898 0.432396940 1.039180549 0.637075235 1.063502938
[31] 0.265507310 1.066961326 1.039989547 0.958572017 1.246700633 0.905354225 1.666109162 0.358623021 0.740307691 1.409810024
[41] 0.125895274 2.233172570 0.595393165 0.794973662


2. Створити фрейм (data frame) y командою y <- data.frame(a = rnorm(100), b
                                                          = 1:100, cc = sample(letters, 100, replace = TRUE)). Для цього data frame
виведіть: останні 10 строк; строки з 10 по 20 включно; 10-й елемент
стовпця b; повністю стовпець cc, при цьому використайте ім’я стовпця.


y <- data.frame(a=rnorm(100), b=1:100, cc=sample(letters, 100, replace = T))
y

a   b cc
1   -0.284133003   1  q
2    0.182095262   2  l
3    0.576987549   3  b
4    1.365258111   4  x
5   -0.571761881   5  g
6   -2.330082632   6  k
7    0.234343086   7  b
8    1.364469778   8  u
9   -1.166601961   9  j
10  -0.854206485  10  y
11  -0.996111731  11  r
12   1.783245537  12  w
13   0.021640365  13  v
14   0.277670262  14  i
15   0.439249455  15  d
16   0.650991471  16  y
17   1.670597947  17  l
18  -0.118904856  18  p
19   0.873269742  19  f
20   0.001384347  20  q

##останні 10 строк

tail(y, 10)

a   b cc
91   0.7072388  91  r
92   0.8964049  92  q
93   0.1001130  93  k
94   0.8010051  94  g
95  -1.4399451  95  t
96   0.3973803  96  c
97   1.3835041  97  s
98  -0.8526739  98  q
99   1.0864921  99  q
100 -0.6988755 100  q

##строки з 10 по 20 включно

y[10:20, ]

a  b cc
10 -0.854206485 10  y
11 -0.996111731 11  r
12  1.783245537 12  w
13  0.021640365 13  v
14  0.277670262 14  i
15  0.439249455 15  d
16  0.650991471 16  y
17  1.670597947 17  l
18 -0.118904856 18  p
19  0.873269742 19  f
20  0.001384347 20  q

## 10-й елемент стовпця b

y$b[10]

[1] 10

##повністю стовпець cc

y$cc

[1] q l b x g k b u j y r w v i d y l p f q m u p p l k c l s s l i z u q s f o u w p c q c q g p y l e o k c r b a r k s j c y
[63] l q f i w w d c r o v l t h r h s h s d v e g m f t f w r q k g t c s q q q
Levels: a b c d e f g h i j k l m o p q r s t u v w x y z

3. Створити вектор z з елементами 1, 2, 3, NA, 4, NA, 5, NA. Для цього
вектору: виведіть всі елементи, які не NA; підрахуйте середнє значення
всіх елементів цього вектору без NA значень та з NA значеннями.


z <- c(1, 2, 3, NA, 4, NA, 5, NA)

##виведіть всі елементи, які не NA

z[!is.na(z)]

[1] 1 2 3 4 5

## підрахуйте середнє значення всіх елементів цього вектору без NA значень

mean(z[!is.na(z)])

[1] 3

##з NA значеннями

mean(z)

[1] NA