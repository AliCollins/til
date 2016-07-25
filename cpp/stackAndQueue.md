# Stacks and Queues

Use of the standard library stack and queues:
```C++
#include <stack>
#include <queue>

using namespace std;

class Solution {
    //Write your code here
    std::stack<char> st;
    std::queue<char> qu;
    
    public:
        void pushCharacter(char ch) {
            st.push(ch);
        }
        void enqueueCharacter(char ch) {
            qu.push(ch);
        }
        char popCharacter() {
            char c = st.top();
            st.pop();
            return c;
        }
        char dequeueCharacter() {
            char c = qu.front();
            qu.pop();
            return c;
        }
};
```
