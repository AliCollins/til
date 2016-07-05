# Array of Arrays

In order to create an array of arrays of integers (where each child array could be of different sizes), see the following C++ code:

```cpp
int **data = new int*[n];
// Data Input
for(int i = 0; i < n; i++) {
    int c, x;
    cin >> c;
    data[i] = new int[c];
    for(int j = 0; j < c; j++) {
        cin >> x;
        data[i][j] = x;
    }
}
...
// Data Clear-up
for(int z = 0; z < n; z++) {
    delete [] data[z];
}
delete [] data;
```
