# Is-a-number-prime-
Program that has a function that returns a Boolean value True if the function's argument is a prime number, else the function returns False.

def is_prime(num):
		# A prime number is a positive integer value with only two factors; factors being one and the number itself
		# All integers less than or equal to one are not prime numbers based on the above definition
    if num <= 1:
        return False
		
		# Two is the first prime number
    elif num == 2:
        return True
		
		# For prime numbers greater than two
    else:
				# e represents the square root of the is_prime function argument num. This value (e) indicates the highest factor of the argument num
        e = int((num**0.5) + 1)
        if e > 2:
						# This program checks if num has any factors between 2 (included) and e (excluded), if a factor(s) exist, then one, the factors(s) and the number itself are factors of num, implying that num is not a prime number
            for i in range(2, e):
                if (num % i) == 0:
                    return False
						# if no factors were found within the two to e range, then num is a prime number
            else:
                return True
				# This program return True because e is less than two and num is greater than both 1 and 2. If num equals four, then e equal 2. Since e is less than 2, then num must be less than 4 and since num is greater than 1 and 2, then the only integer that satifies the code below is three
        else:
            return True
