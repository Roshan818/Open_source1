# Roshan Kumar
## 200104093

### Schedule
|Event Name|Event Date|Gone through resources|
|:--------:|:--------:|:--------------------:|
|Open Source|10/05/2021|YES|
|Competitive Coding|11/05/2021|YES|
|Design|12/05/2021|NO|
|Game Development|13/05/2021|NO|
|Web Development|14/05/2021|YES|
|Machine Learning|15/05/2021|YES|
|App Development|16/05/2021|NO|

### Program Code
```
#include <iostream>
#include <string>
#include <vector>
using namespace std;

long long int ASCII(string str,vector<long long int>& sumArr)
{ 
    int l = str.length();
    int sum = 0;
    long long int TotalSum = 0L;
    for (int i = 0; i < l; i++)
    {
        if (str[i] == ' ')
        { 
            TotalSum += sum;
            sumArr.push_back(sum);
            sum = 0;
        }
        else            
            sum +=  str[i];       
    }
    sumArr.push_back(sum);
    TotalSum += sum;
    return TotalSum;
}



int main()
{
    string str = "Roshan";
    vector<long long int> sumArr;     
    long long int sum = ASCII(str, sumArr);    
    cout << endl  << "Sum of ASCII values -> " << sum;
    return 0;
}
```
