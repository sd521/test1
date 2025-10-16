def generate_fibonacci(n):
    """生成前n个斐波那契数"""
    if n <= 0:
        return []
    elif n == 1:
        return [0]
    
    fib_sequence = [0, 1]
    for i in range(2, n):
        next_num = fib_sequence[i-1] + fib_sequence[i-2]
        fib_sequence.append(next_num)
    
    return fib_sequence

if __name__ == "__main__":
    try:
        count = int(input("请输入要生成的斐波那契数的数量: "))
        if count < 0:
            print("请输入一个非负整数")
        else:
            fib_numbers = generate_fibonacci(count)
            print(f"前{count}个斐波那契数是:")
            print(fib_numbers)
    except ValueError:
        print("请输入有效的整数")
    
