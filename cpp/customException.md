# Create a custom Exception

```c++
class BadLengthException: public std::exception {
    private:
        const int n;
    public:
        BadLengthException(int n) : std::exception(), n(n) {
        }
        virtual const char* what() const throw() {
            stringstream ss;
            ss << n;
            return (ss.str()).c_str();
        }
};
```
