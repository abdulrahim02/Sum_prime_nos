# Sum_prime_nos
Created by Abdulrahim Mulla


//Sum_prime_nos
#include <iostream>
using namespace std;
int func(int num);

int main()
{
	int num , i;
   cout << "Enter a number : \n";cin >> num;
   
   for(i = 2; i <= num/2; ++i) 
   {
      if (func(i)) 
	  {
         if (func(num - i)) 
		 {
            cout << num << " = " << i << " + " << num-i << endl;
         }
      }
   }
   return 0;
}


int func(int num)
{
	int i;
	int f = 1;
	for(i = 2; i <= num/2; ++i) 
	{
      if(num % i == 0) 
	  {
         f = 0;
         break;
      }
   }
   return f;
}
