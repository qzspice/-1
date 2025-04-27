import time
import random

Yourscore = 0
Computerscore = 0
while Yourscore < 3 and Computerscore < 3:
 print("счёт:" + str(Yourscore) + ":" + str(Computerscore))
 you = input("выберите: камень / ножницы / бумага")
 if you == "камень" or you == "ножницы" or you == "бумага":
  comp=random.randint(1, 3)
  if comp == 1:
    comp = "камень"
  elif comp == 2:
    comp="ножницы"
  else:
    comp = "бумага"
  print("камень, ножницы , бумага")
  time.sleep(1)
  print("3...")
  time.sleep(1)
  print("2...")
  time.sleep(1)
  print("1...")
  time.sleep(1)
  print("компьютер выбрал:" + comp)
  if comp == you:
    print("ничья")
  elif you == "камень" and comp == "ножницы":
    print("вы выиграли")
    Yourscore = Yourscore + 1
  elif you == "ножницы" and comp == "бумага":
    print("вы выиграли")
    Yourscore = Yourscore + 1
  elif you == "бумага" and comp == "камень":
    print("вы выиграли")
    Yourscore = Yourscore + 1
  else:
    print("вы проиграли")
    Computerscore = Computerscore + 1 
 else:
   print ("Нет такого варианта")
time.sleep(1)
print("игра закончилась")
print("итоговый счет:" + str(Yourscore) + "-" + str(Computerscore))
