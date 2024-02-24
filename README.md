# sieve-of-eratosthenes

main_list=list(range (4,151))
prime_list=[2,3]

def is_prime(num):
    '''return True if num is a prime number '''
    if(num%2 & num%3 == 0):
        if (num != 2):
            return False
    return True


def sieve_of_eratosthenes(number):
    global main_list
    for num in main_list:
        if is_prime(num):
            prime_list.append(num)

            main_list=[x for x in main_list if x % num != 0]


sieve_of_eratosthenes(5)
print("the numbers of Prime numbers found is :", len(prime_list) , " there are:", prime_list)







