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
