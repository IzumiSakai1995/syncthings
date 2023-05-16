```cpp
int main() {
	// length of output string is 9
	int length_of_output = 9;
	string str = "s001";
	str.insert(1, length_of_output - str.size() - 1);
	cout << str << endl; // s00000001
}
```