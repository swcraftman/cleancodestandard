# Clean code standard

## Purpose: 

illustrate what's 'clean code' to develop teams, recommend clean code practices in daily work ???enterprise SW development requires maintainability ???

## Objective: 

(SMART referred) specific, measurable, attainable, etc ???
tips Principle: no surprise, decrease burden of readers, explicit, ???

## Requisite

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

## Recommended

## Suggestion
