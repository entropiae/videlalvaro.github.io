---
layout: post
title: Metaphors We Compute By
---
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:site" content="@old_sound">
<meta name="twitter:creator" content="@old_sound">
<meta name="twitter:title" content="Metaphors We Compute By">
<meta name="twitter:description" content="How metaphors affect our code.">
<meta name="twitter:image" content="http://alvaro-videla.com/images/computer_chip.jpg">

# {{page.title}}

<span class="meta">January 17 2017</span>

In the book Metaphors We Live By, George Lakoff and Mark Johnson set
out to show the linguistic and philosophical worlds that metaphor
wasn't just a matter of poetry and rhetorical flourish. They showed
that metaphor permeates all areas of our lives, and in particular that
metaphor dictates how we understand the world, how we act in it, how
we live it. They showed our conceptual system is based on metaphors
too, but since we are not normally aware of our own conceptual system,
they had to study it via a proxy: language.

![computer chip](/images/computer_chip.jpg)

## In the beginning there was the Word ##

By studying language they tried to understand how metaphors work by
imposing meaning in our lives. The basic example they present is the
conceptual metaphor of "Argument is War". We understand the act of
arguing with another person in the same way we understand wars. This
means we come up with the following expressions in our daily language:

- Your claims are _indefensible_.
- He _attacked every weak point_ in my argument.
- I _demolished_ his argument.
- I never _won_ an argument with him.

The problem with these sentences that seem innocuous is that we act
and feel based on them. We end up seeing the person we are arguing
with as our _opponent_. Someone that's attacking our positions. This
mean we structure argument in a similar way as if we were at war with
the other person. This means the metaphor is not just language
flourish, we live it. Lakoff and Johnson propose the exercise of
imagining a culture where arguments are not viewed in terms of war, of
winners and losers, but in which language is a dance, where we have to
cooperate with our partner in order to achieve our desired goal,
reaching conclusions as a team. The book keeps going analyzing the
different aspects of language and metaphors and how they affect our
concepts and view of the world. Many examples are given in order to
defend their thesis that we understand the world in term of metaphors
and that we base our most basic behaviors on those metaphors.

What's very important to understand from the book is that metaphors
enable certain ways of thinking while it restrict others, as the
example above shows. In this article we are interested in
understanding how metaphors shape the way we understand computing and
its related problems. We want to see what kind of problems are enabled
by the metaphors in use, and for which ones we lack the right
metaphors still. And no, monads are not like burritos!

In what follows we are not going to discuss the book thesis any
further, on the other hand, we will accept it and bring it into
Computer Science. First we will see how metaphor help us understand
the world of computers, a world that didn't exist a mere 80 years
ago. Then we will try to see how metaphor works in the way we
structure code, or design algorithms and data structures. We will see
that we even face problems in our discipline based on what metaphors
are part of our arsenal.

>"Sometimes our tools do what we tell them to. Other times, we adapt
>ourselves to our tools' requirements." -- The Shallows. Metaphors are
>the tools of comprehension.

## A metaphorical understanding ##

We understand new concepts by way of relating them to things we
already know. Back in the late '40s and early '50s when today's
computers came to life, there was no word to name such invention, but
we understood them as automatic brains. What's more interesting is the
fact that the word _computer_ existed already, and it was the term
used to refer to the person doing calculations for engineers. Think of
an engineer having to know what would be the trajectory of a
projectile, or how the wind would affect an airplane wing shape, so
they would throw a couple of formulas and numbers to their "human
computers" in order to get the answer they wanted. Now they had these
new machines that worked automatically, so they called them Electronic
Computers, dropping the electronic part as timed passed by. So our
very own discipline was named after a metaphor.

But metaphors also obscure possibilities if we don't understand their
limitations. A common problem with new metaphors is that we use the
original meaning of the word at face value. We don't pay attention to
how the word we are using to explain a new concept limits our
understanding of the very concept we are trying to explain. James
Gleick on his book The Information gives a fascinating account of the
invention of the telegraph. The word "tele-graph" means
far-writing. Lo and behold early telegraphs were strange machines that
tried to actually write at a distance, using one-to-one mapping of
letters of the alphabet into wires which sounds terribly
impractical. Around that time, thanks to Braille we understood that
language could be coded in a form different from how it sounds (or
written). Morse Code was the next step to improve our telegraphs, and
to understand that we don't have to write-at-a-distance to have actual
long distance communications. Thanks to Claude Shannon and the many
smart people before him, we managed to escape from the problems of the
_telegraph_ direct metaphor and build whole discipline of Information
Theory. We know that information must be encoded first, then sent into
a channel, to be decoded at the other end of the channel so the
destination receives it.

## Metaphors and Code ##

[Charles Baker](http://history.computer.org/pioneers/baker.html) in a
letter to Donald Knuth said that _to program is to write to another
programmer about our solution to a problem_. A program is our
explanation of how a problem might be solved, it's a metaphor that
stands in place of our understanding, but for metaphors to be
effective they need to convey meaning using concepts already known to
us. We could use the explanatory power of a particular program as
measure of its own elegance.

Let's think about the following example. We could program a computer
to command other computers to perform tasks respecting their arrival
order. This description is already hard to understand. On the other
hand we could describe the solution by talking of a _Queue Server_
that assigns _Jobs_ to _Workers_ based on _a First Come First Served_
queue discipline. Queues are a familiar concept from our daily lives,
we see them at the supermarket or the bank. We wait in them at
airports or train stations. We understand how they work, so for
someone reading our code it might be easier to talk about queues,
workers and jobs, than to go all over the verbosity required to
explain this setting without using the _Queue_ metaphor. We see that
by choosing the right metaphor our program reaches a level of
abstraction that requires the least effort for someone foreign to the
problem to understand our solution. Also by solving our problem with
queues, we get a whole mathematical theory for free. We are no longer
punching blind in the dark. Now we can analyze and understand our
problem with all the tools provided by Queueing Theory.

## Data Structures as Metaphors ##

We analyze data structures to see which one would be a better fit for
the performance characteristics of our particular problem, but we
often forget that a data structure also contains explanatory power.

The choice of data structures helps us convey the meaning. We could
store a bunch of elements in an array, but what if we actually need to
ensure that the elements are unique? Isn't that what _Sets_ are for?
The underlying representation of our set can still be backed by a
plain array, but now our program express its intentions in a clearer
way. Whenever another programmer reads it, they will understand that
the elements in our collection must be unique. A very important
realization is to see that for a computer our programs will be just
another succession of bits that it needs to process. It is us that
give meaning to those bits, so we have to use the right metaphor on
top of them to make our programs clearer. As it is said:

>no one has seen a program which the machine could not comprehend but
>which humans did. –– Unknown author, although it might be Charles Baker. See [here](http://alvaro-videla.com/2014/09/a-programmers-role.html) for the paper with the original quote.

The same way a metaphor enables certain ways of understanding and
limits others, so do data structures. We saw already saw the problem
with using direct metaphors like the original telegraph. When it comes
to data structures we can see that a Set will tell us that its
elements are unique, and it would allow us to test if an element is a
member of the set. But a Linked List gives us the idea of traversing
its elements on after the other, without being able to skip them. An
Array gives us the idea that we can address its elements by index. The
same can be seen with Queues and Stacks, two of the most fundamental
data structures taught in any algorithms course. Both can be
implemented using an array, the difference is that one returns the
elements in FIFO order, while the other does in LIFO order
respectively. Even if this looks like an everyday thing for most
programmers, the moment we choose to use a Stack instead of a Queue,
we are deciding how we want to explain our program. The Stack is a
very good metaphor for the collection of items that our program works
with, because it tells a future reader of our program in which order
we expect to process the items. We don't even need to read how the
stack is implemented, since we can assume we will get the items in
LIFO order. This is why types are so important in computer
science. Not types as in static type checking of programs, but the
types as the _concepts_ we use to describe our programs: Persons,
Users, Stacks, Trees, Nodes, you name it. Types are the characters
that tell the story of our programs, without types, we just have
operations on streams of bytes.

## Cognitive Leaps ## 

A situation we will face once and again is finding the right metaphor
that describes and explains our problem. As we saw earlier with our
queueing theory example, we had to make a cognitive leap to go from
tasks that we have to process in certain order to understanding this
is a queueing problem. Once we managed the cognitive leap, all the
mathematical tools from queueing theory were at our disposition. Graph
Theory is filled with examples of mundane tasks that once converted to
a graph problem, have well known solutions. Whenever you ask Google
Maps to get you to your destination, Google is translating your
problem to a graph representation.  Graphs are the right metaphor,
understood by mathematicians and computers alike. Do we have more
instances of problems that seem difficult but that we crack once we
find the right metaphor? The Distributed Systems literature has a very
interesting one.

In the late '80s Alan Demers and his colleagues from Xerox tried to
find a solution to database replication in unreliable networks. They
classified their algorithms as "randomized", explaining them by using
the _Rumor Mongering_ metaphor: a computer would tell two other
computers about and update, then each in turn will tell two other
computers about the update, and so on, until the information got
replicated. This metaphor gave way to a new area of study called
around so called _Gossip Algorithms_. The _gossip_ metaphor makes the
idea easy to explain, but we still lack the mathematical tools that
would help us analyze the effectiveness of the algorithms. During
their research they discovered another metaphor related to
Epidemics. They understood that their algorithms replicated data like
when an epidemic disseminated across a population. By using this new
metaphor they got immediate access to all the knowledge
in
[The Mathematical Theory of Epidemics](https://www.amazon.com/Mathematical-Theory-Epidemics-Norman-Bailey/dp/0852641133),
which fitted their work like a glove. Not only they named their paper
"Epidemic Algorithms for Replicated Database Maintenance" but they
also took the nomenclature of the discipline to explain their
algorithms. It was a matter of finding the right metaphor to get
access to a new world of explanatory power.

## Metaphors Everywhere ##

We might still be skeptical and ask ourselves if we do use that many
metaphors in programming. Let's take a look at the Distributed Systems
literature in general (metaphors are in _italics_):

Whenever nodes need to _agree_ on a common value, we start a
_consensus_ algorithm to decide on a value. There's usually a _leader_
process that takes care of making the final decision based on the
_votes_ it has received from its _peers_. Nodes communicate sending
_messages_ over a _channel_, which might get _congested due to too
much traffic_. This could create an information _bottleneck_, with
_queues_ at each end of the _channels_ backing up. These bottleneck
might render one or more nodes unresponsive, causing _network
partitions_. Is the process that's taking long to _respond dead_? We
won't know unless we set a timeout. I could go on, but I guess you get
the point.

## A Story in Code ##

As programmers we must be able to tell a story with our code
explaining how you solved a particular problem. Like a writer we must
know our metaphors. Many metaphors will be able to explain a concept,
but we must have enough skill to choose the right one that's able to
convey our ideas to those future programmers that will read our
code. Thus we cannot use every metaphor under our belt. We must master
the art of metaphor selection, of meaning amplification. We must know
when to add and when to subtract. We will learn to revise and rewrite
our code like a writer does. Once there's nothing else to add or
remove we have finished our work. The problem we started with is now
the solution in front of our eyes. Is that the meaning we intended to
convey in the first place?

## References ##

- Lakoff, George, and Mark Johnson. "Metaphors We Live By"
- Gleick, James. "The Information: A History, a Theory, a Flood"
- Shannon, Claude Elwood, and Warren Weaver. "The Mathematical Theory of Communication."
- Bailey, Norman T. J. "The Mathematical Theory of Epidemics" 
- Demers, Alan, Dan Greene, Carl Hauser, Wes Irish, and John Larson. "Epidemic Algorithms for Replicated Database Maintenance"

## Credits ##

Image: [https://flic.kr/p/6GRuVy](https://flic.kr/p/6GRuVy) License [CC BY-NC 2.0](https://creativecommons.org/licenses/by-nc/2.0/)
