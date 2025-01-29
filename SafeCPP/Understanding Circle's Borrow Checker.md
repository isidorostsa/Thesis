# Interesting example

This code compiles. This is because reassigning `views` signals that we don't care about `s` being invalidated.

```c++
int main() safe {
  vector<string_view> views {};

  // views contains s
  string s("Str object");
  views^.push_back(s);

  // views reference of s is invalidated
  s^.append("-------------------------------------");

  // views stops caring about s
  views = {"123"};

  for(auto i : views) {
    println(i);
  }
}
```

If we did not reassign this would not compile.

