1. Introduction
	- Infra depends on C++, but C++ needs to be safer
2. Background and Related work
	- What is programming language Safety
	- Existing solutions
		- Constraint of solutions
			- Cannot rewrite billions LoC
			- New code must be safe
			- Old code must be usable
			- No new bugs must be introduced at the seams
		- Current solutions
			- Profiles
			- Contracts
			- Static/Runtime analysis
			- Cpp-Front
			- Rust
		- Shortcomings of current methods
	- What is Safe-C++
3. Methodology
	- Problem
		- Safe-C++ code should interoperate with old C++ code, without much friction.
	- Solution
		- Discuss possible solutions
			- unsafe-blocks
			- unsafe-types
			- wrappers in the style of https://godbolt.org/z/rrMYn8a4G
		- Describe generic steps of creating a Safe-C++ wrapper
			- Safe-C++ functions are more restrained than C++. Wrapping C++ funcs may take away from their functionality, to guarantee safety.
				- Example: `swap(T& a, T& b)` wrapped with `swap(T^ a, T^ b)`. This does the same thing almost always, but single aliasing borrows force $a \neq b$
		- Form plan for wrapping case study library (HPX)
			- **Can I explore safe parallelism too in the scope of the thesis?**
4. Evaluation of case study wrapper
	- Examples of using the wrapped library
		- Example Safe-C++ application
	- Explore possible bugs in wrapping, bugs happen at the seams
	- Static metrics of code quality/readability
	- Showcase possible bugs prevented
	- **Survey around usefulness/Usability of wrapper**
5. Conclusion
	- Achieved relative safety and protection from common bugs
		- Compatibility with a wider ecosystem.