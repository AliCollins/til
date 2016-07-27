# Generics

Example of using generics (a function template operates with generic types):

```C++
template <class T>
void printArray(vector<T>& v) {
    for(T i: v) {
        cout << i << endl;
    }
} 
```
