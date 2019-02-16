def checkPrime(num):
    isprime = True 
    for i in range(2, num):
            while isprime:
               if (num % i) == 0:
                   isprime = False
                   break
               else:
                   isprime = True
                   break;
    return isprime  


a, b = map(int, input("Enter a and b for [a,b]: ").split())
d = int(input("Enter the difference of two primes: "))

flag = False;
for num in range(a,b-d+1):
    if (flag):
        break
    #Check for first prime
    for i in range(2,num):
        if (checkPrime(num)):
            p = num
            q = p + d
            #Check if (first prime + d) is prime
            if (checkPrime(q)):
                print("The first pair of primes in [",a,",",b,"] with difference",d,"is (",p,",",q,")")
                flag = True;
                break

           