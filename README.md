# scientific-domain-design-resources

I created this as a resource to hold my thoughts, observations and experiences with focusing on capturing domain into a machine rather than think about programming specific ideas or patterns. I believe that premature abstraction and optimizations are the greatest evils in programming and are a waste of time. In contrast to over-engineering with premature abstraction, capturing your domain to represent accurately in code and thinking of experiments and tests that validate your code/programs are never a waste of time.

# Functional programming structure

I've identified that a good way to represent domains is to categorize things within a domain as `DomainModels`, `DomainRules`, `PureCalculations`, `ImpureCalculations`, and `InternalFunctions`.  Using that structure, I've been finding that I can basically represent any world or domain that I've come across in existence so far whether they be real or imaginary.

# Visualization

I think a good place to start is to imagine that you intend to write a library for a specific purpose or domain. You want to first identify a DomainModel in there and establish a DomainRule. Put yourself in the shoes of a domain expert. We want to be able to encapsulate a domain expert into machine code. To be able to give a machine clear instructions, an expert would start to imagine how to give a little child with infinite pen and paper and lives in a box and can only communicate through streams of letters and numbers how to think about the domain (Church-Turing thesis). When trying to explain to a child a domain, an expert will naturally mentally think about mental domain models and rules of the domain. Code can interface with systems that don't behave the same way all the time, the act of interfacing can be called "ImpureActions." Code that is made to calculate a value or determine a decision can be called "PureCalculations." ImpureActions and PureCalculations should use DomainModels and DomainRules in way that benefits the intended user. A person should be able to read domain models and rules and be able to figure out the domain. A person should be able to read ImpureActions and PureCalculations code and associated tests to understand how it is intended for a user to use the domain.

Unit tests would most likely be written for PureCalculations with the mindset of "how would I verify that a domain expert is encapsulated in this code?" Integration or end to end tests would be more useful to verify ImpureActions working and behaving as expected.
