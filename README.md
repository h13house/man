import random

def guess_number_game():
    # 生成一个1到100之间的随机数
    number_to_guess = random.randint(1, 100)
    attempts = 0
    guessed_correctly = False

    print("欢迎来到猜数字游戏！")
    print("我已经想好了一个1到100之间的数字，你猜猜是多少？")

    while not guessed_correctly:
        try:
            # 获取玩家输入
            guess = int(input("请输入你猜的数字: "))
            attempts += 1

            if guess < number_to_guess:
                print("太低了，再试一次！")
            elif guess > number_to_guess:
                print("太高了，再试一次！")
            else:
                guessed_correctly = True
                print(f"恭喜你！你猜对了！你用了{attempts}次尝试。")
        except ValueError:
            print("请输入一个有效的数字！")

if __name__ == "__main__":
    guess_number_game()