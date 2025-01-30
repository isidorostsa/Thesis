1. Introduction
	- Infra depends on C++, but C++ needs to be safer
2. Background and Related work
	- What is Memory Safety
	- How can we achieve it
		- What is being done on that front
			- Profiles
			- Contracts
			- Static/Runtime analysis
		- Shortcomings of current methods
	- What is Safe-C++
3. Methodology
	- Problem
		- Safe-C++ needs access to vast existing code through wrappers
	- Solution
		- Describe generic steps of creating a Safe-C++ wrapper
		- Describe the plan for wrapping case study library (HPX)
			- **Keep old interface?**
4. Evaluation (of case study library)
	- Examples of using the wrapped library
	- Compare wrapping vs rewriting
	- Explore possible bugs in wrapping, bugs happen at the seams
	- Static metrics of code quality/readability
	- Showcase possible bugs prevented
	- **Survey around usefulness/Usability of wrapper**
5. Conclusion
	- Achieved relative safety and protection from common bugs
	- Compatibility with a wider ecosystem.
