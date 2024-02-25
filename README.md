# sieve-of-eratosthenes

main_list=list(range (4,151))
prime_list=[2,3]

### this is not how you check if a number is prime
def is_prime(num):
    '''return True if num is a prime number '''
    ### this is not the correct syntax for multiple conditions. write more for more clearaty
    ### if(num2%3===0 and num3%3==0)
    if(num%2 & num%3 == 0):
        if (num != 2):
            return False
    return True


def sieve_of_eratosthenes(number):
### this is not the algorithm
    global main_list
    for num in main_list:
        if is_prime(num):
            prime_list.append(num)

            main_list=[x for x in main_list if x % num != 0]


sieve_of_eratosthenes(5)
print("the numbers of Prime numbers found is :", len(prime_list) , " there are:", prime_list)
### missing 5, 25 is in the prime list and is not prime, 55, 115...







