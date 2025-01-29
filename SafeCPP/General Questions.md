
There is this snippet in the video:

```c++
template<std2::send F, std2::send... Args>
thread/(where F:static, Args...:static)(F f, Args... args) safe {...}
```

`Args` are types, but the `where` restrictions apply to the lifetime of objects. Does this only work where each type corresponds to exactly one input parameter?

---

The following snippet from the video does not compile under `build_226`.

```c++
#feature on safety  
#include <std2.h>  
  
using namespace std2;  
  
void entry_point (const string^ s, int a) safe {  
  println(*s);  
}  
  
int main() safe {  
  vector<thread> threads {};  
  
  {  
    string s("Hello");  
    const int num_threads = 15;  
    for (int i: num_threads) {  
      threads^.push_back(thread(&entry_point, ^const s, i));  
    }  
  }  
  
  for(thread^ t : ^threads) {  
    t^->join();  
  }  
}
```

It gives the following error, which is different from the one presented in the video.

```text
error: main.cxx:22:13
    t^->join(); 
            ^
no viable candidates in call to join
  object is prvalue std2::thread^
  candidate: std2.h:1603:8
    void join(self) safe { 
         ^
    error: main.cxx:22:13
        t^->join(); 
                ^
    could not bind explicit object parameter std2::thread to prvalue std2::thread^
```

