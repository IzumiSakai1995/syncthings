
## sorting

```cpp
//
// Created by liuzheng on 2022/11/1.
//

// sort map

#include <iostream>
#include <map>

// method1 : using the vector of pair
// copy all contents from the map to the corresponding vector of pairs
// and sort the vector of pairs according to second value using the lambda function given below

using namespace std;

bool cmp(pair<string, int> p1, pair<string, int> p2) {
    return p1.second < p2.second;
}

// Comparator function to sort pairs
// according to second value

// Function to sort the map according
// to value in a (key-value) pairs
void sort(map<string, int>& M)
{

    // Declare vector of pairs
    vector<pair<string, int> > A;

    // Copy key-value pair from Map
    // to vector of pairs
    for (auto& it : M) {
        A.push_back(it);
    }

    // Sort using comparator function
    sort(A.begin(), A.end(), cmp);

    // Print the sorted value
    for (auto& it : A) {

        cout << it.first << ' '
             << it.second << endl;
    }
}

// Driver Code
int main()
{

    // Declare Map
    map<string, int> M;

    // Given Map
    M = { { "GfG", 3 },
          { "To", 2 },
          { "Welcome", 1 } };

    // Function Call
    sort(M);
    return 0;
}
```

