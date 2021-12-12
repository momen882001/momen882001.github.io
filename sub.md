# Constant and Ampersand Report

![An image about how to declare constants](https://media.geeksforgeeks.org/wp-content/uploads/20201223212505/t1.png)

![An image about pointers with constants](https://www.geeksforgeeks.org/wp-content/uploads/PointersWithConstants-768x401.png)

1.  _The pointer variable point to a const value:_
    Syntax:
    **const data_type\* var_name;**
    code :
    int main()
    {
    int x{ 10 };
    char y{ 'M' };
    const int* i = &x;
    const char* j = &y;

            x = 9;
            y = 'A';

            cout << *i << " " << *j;
        }

    Explanation:
    In the example above, I and j are two pointer variables pointing to memory locations of type const int-type and char-type, respectively, but the value stored at these corresponding locations can be altered as shown above.

2.  _The const pointer variable point to the value:_
    Syntax:
    **data_type\* const var_name;**
    code :
    int main()
    {
    int x = 5;
    int z = 6;
    char y = 'A';
    char p = 'C';

            int* const i = &x;

            char* const j = &y;

            *i = 10;
            *j = 'D';

            cout << *i << " and " << *j
                << endl;
            cout << i << " and " << j;

            return 0;
        }

    Explanation:
    The values that are stored in the corresponding pointer variable i and j are modifiable, but the locations that are pointed out by const-pointer variables where the corresponding values of x and y are stored aren’t modifiable.

3.  _const pointer pointing to a const variable:_
    Syntax:
    **const data_type\* const var_name;**
    code :
    int main()
    {
    int x{ 9 };
    const int\* const i = &x;

            char y{ 'A' };

            const char* const j = &y;

            cout << *i << " and " << *j;

            return 0;
        }

    Explanation:
    Here, the const pointer variable points to the const variable. So, you are neither allowed to change the const pointer variable(*P) nor the value stored at the location pointed by that pointer variable(*P).

## Usages of **&** operator :

1. _take the address of a variable :_
   code :
   int x;
   void\* p = &x;

2. _pass an argument by reference to a function :_
   code :
   void foo(CDummy& x);
   void fooconst(const CDummy& x);

3. _declare a reference variable :_
   code :
   int k = 0;
   int& r = k;
   r = 3;
   assert( k == 3 )

4. _bitwise and operator_
   code :
   int a = 3 & 1 ;
