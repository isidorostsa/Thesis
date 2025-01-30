Write a small document explaining to Sean what I want to do and what I would like from him.

I want to:
- Write wrappers around some hpx facility (probably `hpx::thread` or one of our data structures if adding parallelism is too much)
- Document and assess the difficulty of wrapping existing code.
- Contrive examples of bugs that are prevented by Safe-C++
- Document and evaluate the usability of using the lifetime-annotated code, in a way that interoperates with existing c++ code.
- Write a small safe application that uses the annotated code

What I want from Sean:
- I have a couple of questions:
	- Q: What is the minimum subset of the extra features of `circle` that I can use to cover `hpx::thread`.
	- Q: What would be most helpful to your efforts?
	- Q: "Unlike in Rust, _unsafe-blocks_ do _not_ open new lexical scopes." That seems a little curious. In the [example](https://safecpp.org/draft.html#unsafe-block) you show how you can declare a variable within an unsafe block, and then read form it outside the block.
- Feedback on the topic of the thesis, the direction, and technical part.
- A small cheat-sheet of what the circle syntax constructs map to rust.












