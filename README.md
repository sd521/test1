# test1
def generate_fibonacci(n):     """生成前n个斐波那契数"""     if n &lt;= 0:         return []     elif n == 1:         return [0]          fib_sequence = [0, 1]     for i in range(2, n):         next_num = fib_sequence[i-1] + fib_sequence[i-2]         fib_sequence.append(next_num)          return fib_sequence
