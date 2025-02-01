# Reading Notes

What is an interpreter?
* ***Gives meaning to random characters** (letters, numbers, special characters)
    * Makes sense out of nonsense
* Acts as the translation layer between humans and computers - computers can only understand 1s and 0s; yet with an interpreter, the characters we type are understood and actioned up by the computer to execute the logic we want

Types of Interpreters
* (low end) Really small, don't include a *parsing* step
    * ie `brainfuck` https://minond.xyz/brainfuck/
* *Parse source code, build an AST, then evaluate the AST (aka "tree-walking" interpreter)
	* Note: This is the style we're building in the book
* *(high end) Optimized using advanced parsing and evaluation techniques
    * TODO: If an AST is not used, what're the alternatives? Why are they preferred? In what use-cases are they warranted?

Interpreter vs Compiler
* An interpreter:
    1. take source code
	2. evaluate the source code without producing a visible, intermediary result 
	3. ^ which can later be executed
* A compiler:
    1. takes source code
    2. produces output in another language
    3. ^ which an underlying/lower-level system understands

Components/entities of an interpreter:
    1. lexer\
    2. parser\
    3. abstract syntax tree\
    4. internal object system\
    5. evaluator

# Questions
1. What are the heuristics for when a programming language implements both an intepreter and a compiler or just one of them?

# Personal Thoughts
* I like that we're only planning to use the std lib - no 3rd party tooling. Excited to explore/get more comfortable with Rust's std lib. Can't wait to learn more re: what I like, don't like, and identify any potential gaps compared to Go's std lib.

# Quotes
> I kept asking myself: how does this work? And the first time this question began forming in my mind, I already knew that I’ll only be satisfied with an answer if I get to it by writing my own interpreter. So I set out to do so.

> What I wanted was something between the 900 page book on compilers and the blog post that explains how to write a Lisp interpreter in 50 lines of Ruby code.

> Either way, there won’t be any meta- programming tricks to take a shortcut that nobody understands anymore after two weeks and no grandiose object-oriented designs and patterns that need pen, paper and the sentence “actually, it’s pretty easy” to explain.
