# Why the Hate?

C++ is universally considered to be a soul sucking language but why? is it the syntax? Is it because you can easily create bugs with it? Is because nobody can agree on a code style? Is it because it's a constantly moving target due to updates? Is it because people write some truly awful code? Is it because it's a pain in the butt to setup and build? 

Yes.

## Part 1: Syntax

C++ was originally designed as a subset of C which itself is actually fairly readable and relatively easy to understand. C style syntax got so popular it's still being used in a bunch of modern programming languages. However C++ evolved to become its own standalone language and kinda has its own syntax that diverges at lot from C. The problem with that is some C++ features can get pretty ugly, the standard library can be confusing and convoluted and even seemingly simple concepts like a dynamic array is a vector in C++... Like whaaaat? Why? 

It also doesn't help that the language itself changes dramatically over the years. C++11 changed the language at a fundamental level to the point that C++ code written after that barely looks like anything before it. With the introduction of smart pointers, it made fundamental concepts like RAII less prevalent and the use of raw pointer is to be avoided when it was basically the only way to do things prior to C++11. Because of that C++ written 10 years ago looks different to C++ written 1 year ago or even 1 week ago looks different and this makes long term maintenance an absolute living nightmare. C doesn't really change all that much over the years. a 20 year old C code base would pretty much work and look similar to one written yesterday. Not C++. 

That said all programming languages have their own quirks and tricky parts, C++ happens to have at lot of that. I wouldn't say this is an insurmountable obstacle as you can always incrementally refactor the code but it's definitely a lot of work. 

## Part 2: Bugs

Being a lower level compiled language C++ gives you a ton of control. And with control comes problems. Quoting Bjarne Stroustrup the man himself, _"C makes it easy to shoot yourself in the foot; C++ makes it harder, but when you do it blows your whole leg off"_ What he means is that an oopsie in C is probably gonna give you a segfault, memory access violations, program crashes etc... These are serious issues don't get me wrong but most operating systems are pretty good at catching those and recovering from them. C++ has features that, while they make those C-style mistakes less likely, you may also end up with memory leaks, file corruptions, slowing down the entire system and even trigger a whole system crash. If C is a toolbox full of hammers and screwdrivers, C++ is a rack of power tools.  

Now while this sounds pretty bad, you do get used to it after a while and you'll make less and less of those mistakes. I say less, you will still make one here and there but you'll get better at knowing how to find and fix them.

## Part 3: The people

Arguably the worse part of C++. Being such a powerful language that can basically do it all. You'll inevitably find divergent opinions on what makes 'good' C++ code (spoiler: there is none, it's all crap and there is only C++ that works and C++ that blows up your system). Worse, some people like to obfuscate features in plain sight. Open Source code means nothing in C++ land, some people have mastered the art of making their code so hard to read it might as well be closed source. C++ does not enforce the use of a formatter (even though they exist) nor have the community peer pressure nagging you to format your code to a certain standard like in Python's. So if you hate C++ it's probably not your fault.

## Part 4: Building C++

This tends to apply to a lot of older compiled languages. Basically C++ doesn't automagically builds once you're done. How does the compiler knows what goes where? How does it know you have libraries to link? Well it doesn't. If you are a masochist you'd write a stupid long command to instruct it to compile but that's super unreliable and you'll probably suffer mentally after several hundreds of compiles. 

Instead there are intermediate tools that instruct the compiler to do the thing you want it to do. The problem is that everyone have their own sauce. Some use scripting. Some are proprietary and then there's CMake. Oh CMake... If you thought you had enough on your plate you also have to learn to how to script a project build?! Yes you heard it right. 

Why though? 

CMake is what I consider necessary evil as the freedom it can afford cannot be overstated. 

What does it do exactly?

I mentioned above that everyone have their own sauce to build C++ programs. Well CMake helps you generate the build files for whatever people want to build with. CMake makes the codebase portable to almost any IDE, build system and even operating system. Visual Studio? Yup. Rawdog Linux Make files? Of course! Xcode? Sure why not (please no). OBVIOUSLY this comes at the cost of extra complexity and therefore debugging. It also doesn't help that CMake has way too many ways to do the same thing in different ways. Still all of this is well worth the extra time spent configuring the build system. With CMake I have been able to build my OpenGL project both on my Linux laptop and Windows desktop without changing anything at all. 

