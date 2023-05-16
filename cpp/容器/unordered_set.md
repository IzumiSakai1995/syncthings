
## Searching

```cpp
#include <unordered_set>
unordered_set<int> hash_set{1,2,3};
if (auto search = hash_set.find(2); search != hash_set.end()) {
	return true;
}
```