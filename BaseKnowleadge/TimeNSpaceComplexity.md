# Time Complexity
* O(1):
    ```C Sharp
    void Func(int n)
    {
        Console.WriteLine("Hello world!");
    }
    ```
* O(n):
    ``` C Sharp
    void Func(int n)
    {
        for (int i = 0; i < n; i++)
        {
            Console.WriteLine(i);
        }
    }
    ```
* O($n^2$)
    ``` C Sharp
    void Func(int n)
    {
        for (int i = 0; i < n; i++)
        {
            for(int j = 0; j < n; j++)
            {
                Console.WriteLine(i+j);
            }
        }
    }
    ```
* O($log_2n$)
    ``` C Sharp
    void Func(int n)
    {
        for(int i = 0; i < n; i*=2)
        {
            Console.WriteLine(i);
        }
    }
    ```
### Common Compare:
  O(1) < O($logn$) < O(n) < O(n$logn$) 
    < O($n^2$) < O($n^3$) < O($2^n$)

# Space Complexity
* O(1)
    ``` C Sharp
    void Func(int n)
    {
        int a = n;
    }
    ```
* O(n)
    ``` C Sharp
    void Func(int n)
    {
        List<int> myList = new List<int>();
        for(int i = 0; i < n; i++)
        {
            myList.Add(i);
        }
    }
    ```
* O($n^2$)
    ``` C Sharp
    void Func(int n)
    {
        List<List<int>> myList = new  List<List<int>>();
        for(int i = 0; i < n; i++)
        {
            List<int> tempList = new List<int>();
            for(int j = 0; j < n; j++)
            {
                tempList.Add(j);
            }
            myList.Add(i,tempList);
        }
    }
    ```

 
