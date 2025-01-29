1. Introduction
	- Infra depends on C++, but C++ needs to be safer
2. Background and Related work
	- What is Memory Safety
	- How can we achieve it
		- What is being done on that front
			- Profiles
			- Static/Runtime analysis
		- Shortcomings of current methods
	- What is Safe-C++
3. Methodology
	- Problem description
		- Safe-C++ access to vast existing code through wrappers. 
		- Describe generic steps of creating such a wrapper
		- Describe the plan for wrapping case study library (HPX)
	(Maybe describe the plan for using a wrapped library)
4. Evaluation (of case study library)
	- Static metrics of code quality/readability
	- Examples of using the wrapped library
	- Showcase prevented possible bugs 
	- Survey around usefulness/Usability of wrapper
5. Conclusion
	- Achieved relative safety and protection from common bugs
	- Compatibility with a wider ecosystem.