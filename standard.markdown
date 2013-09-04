# Clean code standard

## Purpose: 

This standard

* illustrates what's 'clean code' to develop teams, recommend clean code practices in daily work, 
* is establishing a uniform way for programming C code in 'clean code' way. The uniform standard improves maintainability, readability and quality, 
* concentrates on good design and coding principles, on layout specific issues, and on code commenting, 
* is to be used as a reference when evaluating tools, such as the ones meant for generating, analysing or testing code. 

Maintenance (further development, updating, refactoring and fixing) of existing code takes more effort than the actual coding itself. The original programmer might not be the one doing a maintenance task, and after some months have passed by, even he or she might not remember what some particular piece of code is doing. Uniform coding style is one important factor for reducing the maintenance effort, and therefore, it is vital to know and follow the rules and recommendations given in this standard.

Readability is important also in code inspections and team working on same code. These are easier to carry out when everyone on that team is following the uniform coding standard.

## Scope:

These guidelines are to be applied to all C code implemented after the approval of this standard.

This standard should be followed by the collaborators if they are developing C programs which are intended to be parts of the our product. 

Code written outside the organization (e.g. 3rd party components and open source code (e.g. FreeBSD)) does not need to be conforming to this standard.

Whenever existing code is modified try to update the code regarding to the rules and recommendations outlined in this document. This needs to be considered using common sense and maintenance understanding.

### When to change existing code’s style?  The following needs to be considered:

Totally new functions shall be written using this style guide.

If the code does not have a clear style then at least:

* Writing a new routine: use the new style guide
* When changing about 90% (most of) of the source then also change the last non-style guide parts to standard.
* If the code will be reused by another project, then it is reasonable to change style according to this standard.

?? The standard follows the ANSI C Standard. The current standard for C Programming Language is ISO/IEC 9899:1999. ??


## Objective: 

(SMART referred) specific, measurable, attainable, etc ???
tips Principle: no surprise, decrease burden of readers, explicit, ???

## Items

### Requisite

* Naming (can include Magic numbers, repeated string literals): consistent, domain names preferred.
* Comment
* Small functions, do one thing, in one level abstraction?
* Function parameters order: input, output, followed by in/out if any.
* Header files include order: sack header, PRB header part 1, C/C++ lib header, PRB header part 2 ?
* F/T, FALSE/TRUE usage
* 'n' version of strcpy, sprintf… idiom: strncpy(dest, src, sizeof(dest)-1); dest[sizeof(dest)-1]='\0';
* Use sizeof(var_name) and sizeof(*pointer_var_name) instead of sizeof(var_type)
* NULL parameter check should only be performed on extern arguments, avoid null arguments in internal code by design
* Malloc/free should be symmetrical
* Code structure: duplication, nest loops, nest if-else statement…
* Replace complex if condition test with check fuctions, is_xxx(…), check_yyy(…), use positive name
* Modularity: 1) data+functions in most conditions, 2) independent functions; 3) standalone global variables must be us rarely.
* Segregate os/3rd APIs and business logic in moderation
* File organization: small, uniform, module-oriented…
* File format: Use Unix style '\n', not DOS '\r\n', if non-ASCII characters are emitted (very rare), use utf-8 format. elongs to coding style?
* Unit-testing: 1) must also be 'clean'; 2) help verify design, complex/hard to test code implies poor design. (sective ut)
* Coding message transitions and state-machine in SDL, others in C/C++
* Makefile: illustrate file-dependency relationship, refer to Simon's tech-talk
* Performance excuse: 'static inline', find hot-spots by profiling, modularity benefits locating hot-spots and limiting scope of code needs modified

### Recommended

### Suggestion

##TODO
