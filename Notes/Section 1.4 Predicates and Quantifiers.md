## Main Concepts
## Introduction
Even with the propositional logic in [[Section 1.1 - Propositional Logic |Section 1.1]], it's still hard to properly fully express all mathematical logic. 
To bridge this gap, we use predicates and quantifiers, powerful tools that enable us to precisely describe the scope and properties of objects. 

## Predicates
Predicates are tools that describe the properties of an object in our logic. 
So for example, if I want to communicate that person x is active I can just say: $A(x)$.

>If it helps, you can think of it as a function that returns true if the property exists in the given object, and false if not. 
>If it doesn't help, ignore what I just said completely. 

This also works when we're investigating the properties of a relationship between objects.
So for example, if person x is sending an email to person y, we can represent their relationship using predicate $E(x,y)$. 

To use them, we must define them at the beginning of our proofs to clarify their meaning, and each name should only be used to describe one object or one property.
In other words, if I want to describe that someone is active and someone is in Antarctica, I should not be using A(x) for both. 
The same thing applies to objects, I should not be representing penguins and people with variable x. 
## Quantifiers

While predicates help us describe properties, quantifiers help us quantify these properties over a set.
> Sets are a concept we will cover later, but for now imagine a set simply as a group of non repeating objects. This can be a group of people, group of integers, group of planes, etc.

We will only cover two predicates in this class: "For all" ($\forall$) and "Exists" ($\exists$). 
"For all" will be used to say "Every single object in this set must meet these conditions" while "Exists" will be used to say "At least one object in this set must meet these conditions".

So if I want to communicate "Everybody loves Jerry", I can translate that to "All people love Jerry" where "All people" is our quantifier and "love jerry" is a property people have (or our predicate).
So we can communicate "Everybody loves Jerry" as 
$$ \begin{aligned} \forall x (L(x)) \end{aligned} $$

where $L(x)$ means that person x loves jerry.  

Alternatively, "Someone loves Jerry" or "At least one person loves Jerry" can be communicated as
$$ \begin{aligned} \exists x (L(x)) \end{aligned} $$