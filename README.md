#-main
import random

# 生成一个1到100之间的随机数
number = random.randint(1, 100)

# 初始化游戏次数
games = 10

# 开始游戏
print("欢迎来到猜数字游戏！")
print("你有{}次机会来猜测一个1到100之间的数字。".format(games))

# 游戏进行中
while games > 0:
    # 获取用户输入
    guess = int(input("请输入你的猜测："))

    # 判断猜测是否正确
    if guess == number:
        print("恭喜你猜对了！")
        break
    elif guess < number:
        print("猜的数字太小了！")
    else:
        print("猜的数字太大了！")

    # 每次猜测失败，游戏次数减1
    games -= 1

# 输出游戏结果
if games == 0:
    print("很遗憾，你没有猜对，正确答案是{}。".format(number))
else:
    print("你真是太棒了，答对了！")
