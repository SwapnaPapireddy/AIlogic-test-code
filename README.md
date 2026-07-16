# problem 1

n = int(input("number of records: "))
time_slots = eval(input())

# problem 2

n = int(input("number of readings: "))
n_s_sep_int = eval(input())
k = int(input())
listt = []
m = 1
s = n-k+1
if n == len(n_s_sep_int):
    i = 0
    j = k
    if j <=n and i <= n-4:
        while m<s+1:
            sum = 0
            for num in range(i,j):
                sum = sum+n_s_sep_int[num]
            m = m+1
            listt.append(sum)
            i = i+1
            j = j+1
print(max(listt)) 
# 2 1 5 1 3 2

##problem 3

s = input("Enter the s: ")
char_index = {} 
l = 0
max_non_r_s = 0
for r in range(len(s)):
    char = s[r]
    if char in char_index and char_index[char] >= l:
        l = char_index[char] + 1
    char_index[char] = r
    max_non_r_s = max(max_non_r_s, r - l + 1)
print(max_non_r_s)
