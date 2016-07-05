# Overloading Operators

Example of overloading operators for Complex class

```cpp
//Overload operators + and << for the class complex
//+ should add two complex numbers as (a+ib) + (c+id) = (a+c) + i(b+d)
//<< should print a complex number in the format "a+ib"
Complex operator+(Complex lhs, Complex rhs) {
    Complex res;
    res.a = lhs.a + rhs.a;
    res.b = lhs.b + rhs.b;
    return res;
}

std::ostream& operator<<(std::ostream& os, Complex& c) {
    os << c.a << "+i" << c.b;
    return os;
}
```
