# scientific-expert-design-resources

I created this as a resource to hold my thoughts, observations and experiences with focusing on capturing domain expert into a machine rather than think about programming specific ideas or patterns. I believe that premature abstraction and optimizations are the greatest evils in programming and are a waste of time. In contrast to over-engineering with premature abstraction, capturing your domain or system expert to represent accurately in code and thinking of experiments and tests that validate your code/programs are never a waste of time.

# Functional programming structure

I've identified that a good way to represent domains is to categorize things within a domain as `DomainModels`, `DomainRules`, `PureCalculations`, `ImpureCalculations`, and `InternalFunctions`.  Using that structure, I've been finding that I can basically represent any world or domain that I've come across in existence so far whether they be real or imaginary.

# Visualization

I think a good place to start is to imagine that you intend to write a library for a specific purpose or domain. You want to first identify a DomainModel in there and establish a DomainRule. Put yourself in the shoes of a domain expert. We want to be able to encapsulate a domain expert into machine code. To be able to give a machine clear instructions, an expert would start to imagine how to give a little child with infinite pen and paper and lives in a box and can only communicate through streams of letters and numbers how to think about the domain (Church-Turing thesis). When trying to explain to a child a domain, an expert will naturally mentally think about mental domain models and rules of the domain. Code can interface with systems that don't behave the same way all the time, the act of interfacing can be called "ImpureActions." Code that is made to calculate a value or determine a decision can be called "PureCalculations." ImpureActions and PureCalculations should use DomainModels and DomainRules in way that benefits the intended user. A person should be able to read domain models and rules and be able to figure out the domain. A person should be able to read ImpureActions and PureCalculations code and associated tests to understand how it is intended for a user to use the domain.

Unit tests would most likely be written for PureCalculations with the mindset of "how would I verify that a domain expert is encapsulated in this code?" Integration or end to end tests would be more useful to verify ImpureActions working and behaving as expected.

# Problem solving tiers

When you have a problem statement such as "how can I build a sophisticated spam bot that's as good as a human?" You want to be able to predictably break it down into workable tasks that people can work on. These series of transformational breaking down of a problem I find very useful and incremental and it goes as such.

**Problem -> Compututational Theory components -> Architectural Design with Event Modelling -> Scientific Domain Expert Code Implementation**

These series of thinking in my experience leads to all the important questions being asked and results in really good end product.

An example template that I did can be found here https://github.com/FullstackGJJ/employee-specialty-decoder/tree/main/Haskell where you can see how the `Description.md` housed within a directory to encapsulate a domain is done. I plan to do more in the future in other languages for more examples.

When working with a problem, you can start out by imagining an ideal finalized automated solution. From there, you want to work backwards and take away responsibility that is delegated to the user instead of the solution. As you strip away responsibilities from the solution, you have a roadmap for how you can start from nothing to a complete solution. During building the solution, you want to model out values and data that are computable and build assuming they exist, then make them exist and extract out the domain or start from domain that is responsible for values/data existing.

When developing a domain, you don't necessarily have to only start with breaking down the domain. If you feel stuck or you feel like you have to interact with a machine, feel free to just have sample data to use and start coding to perform actions that a domain expert would want. The most importanat part is that eventually domain expert level thinking that is computable is broken down in a way that can be explained to a child with the associated mental models, rules of thumb, decision making, and actions (because instructions are clearer when you imagine a machine as a child).
