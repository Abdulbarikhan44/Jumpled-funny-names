# Jumpled-funny-names
CWH_tuts119

#Author- Abdul Bari KHAN
#23/12/2021
#Medium Problem 9-jumpled funny names

'''
It's result day at school and not everyone is happy. You decided to make your friends laugh
by jumbling their names to come up with some funny names.

Your program should take the number of names and the names separated by space as input.
Output should be funny names in the same order.
Input:

Enter number of friends:
3

Enter the name of your 3 friends:
Rohan Das
Shubham Agarwal
Ritesh Arora

Output:
Ritesh Das
Shubham Arora
Rohan Agarwal
'''

total_friends=int(input("Enter Number of Friends\n"))
print('Enter name of your friends')

friends=[]
for i in range(total_friends):
    friends.append(input().split(' '))
print(friends)

import random
random_list=random.sample(range(total_friends),total_friends)
print(random_list,"\n")

#loop 5 baar;  if total friends =5
for i in range(total_friends):
    print(friends[i][0], end=" ")                    #printing first name of friends list[0]
    #loop 2 baar agr last_name me 3 word hai
    for j in range(len(friends[random_list[i]]) - 1):     #loop running if last name has more than 1 word.
        print(friends[(random_list[i])][j + 1], end=" ")        #printing last name of friends list[random number]
    print("")           #use to print new line


'''
(first_ name last_name) format:

shafi jafri
farhan alam
maq
huzaifa ahmad zaidi hai
aman akhtar nahi
'''
