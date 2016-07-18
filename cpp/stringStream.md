# StringStream

Parse a vector array of ints from a string input using StringStream:

``` cpp
vector<int> parseInts(string str) {
    vector<int> v;
    stringstream ss(str);
    string token;
    while(getline(ss, token, ',')) {
        v.push_back(stoi(token));  // Taking advantage of C++11 stoi function
    }
    return v;
}

```
