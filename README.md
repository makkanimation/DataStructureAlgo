# DataStructureAlgo
  ## Recursion::
1Q: How to find the sum of digits of a positive integer number using recursion?
Ans:
  a.) 10 : 10/10 = 1 and Remainder =0
  b.) 112 : 112/10 = 11 and Remainder = 2
            11/10  = 1 and Remainder = 1
  c.) f(n) = n%10 + f(n/10)
     function sumofDigits(n)
    {
      if(n==0){
        return 0
      }
      else{
        return (int)n%10 + sumofDigits(n/10)
      }
    }
  
