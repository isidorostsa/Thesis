1. Introduction
	- Infra depends on C++, but C++ needs to be safer
2. Background and Related work
	- What is programming language Safety
	- Existing solutions
		- Constraint of solutions
			- Cannot rewrite billions of LoC
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
			- wrappers
		- Describe generic steps of creating a Safe-C++ wrapper
			- SCpp functions are more restrained than Cpp. Wrapping Cpp functions takes away from their functionality, but guarantees safety. e.g. guarantees no aliasing.
		- Form plan for wrapping case study library (HPX)
			- **Expose safe parallelism in thesis scope?**
			- **Retain the existing interface?**
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