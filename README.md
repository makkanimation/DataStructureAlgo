# DataStructureAlgo
  ## Recursion::
1Q: How to find the sum of digits of a positive integer number using recursion?
Ans:
  a.) 10 : 10/10 = 1 and Remainder =0
  
  b.) 112 : 112/10 = 11 and Remainder = 2
            11/10  = 1 and Remainder = 1
            
  c.) f(n) = n%10 + f(n/10)
  
    ```
    
    function sumofDigits($n)    
    {    
      if($n==0){
        return 0
      }
      else{
        return (int)$n%10 + sumofDigits($n/10);
      }      
    }
    ```

  2Q: How to calculate power of a number using recursion?
  Ans: 
    Xn = X*X*X ..(n times).. *X;

    2^4 = 2*2*2*2;
    
    X^3 * X4 = X^3+4 (X^a * X^b = X^a+b);
    
    so our condition will be like this: X^n = X * X^n-1
    
    ```
    
    function power($base,$exp)    
    {    
      if($exp==0){
        return 1;
      }
      elseif($exp==1)
      {
        Return $base;
      }
      else{
        return $base * power($base,$exp-1);
      }      
    }
    ```

    
  3Q: How to find the GCD(Greatest Common Divisor) of two numbers using recursion?
  Ans: GCD is the largest positive integer that divides the numbers without a remainder
    Euclidean Algorithm

    gcd(48/18);
    Step 1: 48/18 = 2 remainder 12
    Step 2: 18/12 = 1 remainder 6
    Step 3 : 12/16 = 2 remainder 0

      gcd(a,0) = a // Always come, we will return base value
      gcd(a,b) = gcd(b,a mod b)
    
    ```
    
    def gcd(a, b):
    assert int(a) == a and int(b) == b, 'The numbers must be integer only!'
    if a < 0:
        a = -1 * a
    if b < 0:
        b = -1 * b
    if b == 0:
        return a
    else:
        return gcd(b, a%b)
    ```
