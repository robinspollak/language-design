_Fill in each this file with your responses, placing each response after its
corresponding question._

---

**Question**

Pick three quotes from the readings about language design. Good candidates 
are:

   + Something you agreed with / resonates with your own experience
   + Something you disagree with
   + Something that is interesting, a new idea or perspective you'd like to remember
   + Something you didn't understand

For each quote, describe what it was about the quote that led you pick it.

**Response**
# Quote 1, Mernik et all 2002, Section 2.2
>"As mentioned in Section 1.1, a quantitative treatment of the trade-offs involved is difficult. In practice, short-term consid- erations and lack of expertise may easily cause indefinite postponement of the decision." [Mernik et all 2002 section 2.2]

This quote really resonated with us because we realized that doing what is comfortable often leads to not doing what is hard (or has high startup costs) which would potentially deter developers from building a new language to develop in, even if that language might be more comfortable in the long run. We also decided that even though building/designing a DSL is not _that_ hard it does require mental effort almost every step of the way. First you need to decide that its necessary, then you need to make implementation choices etc. When building a large project its sometimes difficult to look past short term considerations (like getting code written) in order to see long term benefits of potentially building a DSL. We also noticed that this quote makes for good life advice: don't postpone hard things because eventually postponing just means not doing. 

# Quote 2, Bloch 2006
>"If it’s hard to find good names, go back to the drawing board.
Don’t be afraid to split or merge an API, or embed it in a more general setting. If names start falling into place, you’re on the right track." [Bloch 2006]

We chose this quote because we agreed with it in some contexts but also thought that it didn't necessarily apply to all cases, situations or project types. We thought that this quote was good advice for building an API (when other people would be using it) but we weren't sure whether it applied to programming larger scale project. It definitely is a really intersting gauge to use and an easy and illuminating question to ask yourself as a devloper in order to get a read on how clear your thoughts are about what you're building and why. The problem we had with it was that we weren't convinced that every useful/necessary thing in a project would have an obvious name. What about helper functions? Those often serve specific and important purposes but don't always have obvious names. Consider the example of binary tree traversal--this relatively simple concept requires helper functions that dont necessarily have obvious names. 

# Quote 3, Steele, 1998
>"But the key point of the bazaar is not that you can get many persons to work with you at a task, for cathedral builders had a great deal of help, too. Nor is the key point that you get help with the designing as well as with the building, though that in fact is a big win. No, the key point is that in the bazaar style of building a program or designing a language or what you will, the plan can change in real time to meet the needs of those who work on it and use it. This tends to make users stay with it as time goes by; they will take joy in working hard and helping out if they know that their wants and needs have some weight and their hard work can change the plan for the better." [Steele, 1998]

We really liked this quote because we definitely agree that helping with design is sometimes more important than helping with building. We did have a question about it though. Isn't it plausible that if many people are helping with design that the project could lose focus? We think its important for a project to have focus even if it has diversity of ideas. This quote seems to conflict with his later point about not cluttering a language with too many primitives. He discusses the possibility of adding complex/rational numbers, intervals etc. as primitives but states that should definitely not happen. "I might say “yes” to each one of these, but it is clear that I must say “no” to all of them! And so would James Gosling and Bill Joy. To add all these types to the Java programming language would be just too much. Some parts of the programming vocabulary are fit for all programmers to use, but other parts are just for their own niches. It would not be fair to weigh down all programmers with the need to have or to learn all the words for all niche uses." [Steele,1998] We agree with this conclusion and think that people should definitely be able to add to their own "fork of the language" by adding libraries, define first class objects, etc. but we dont think that everyone should be able to design the "master fork" of the language. The analogy Steele uses later of a shopping mall resonated with us because it called both for customizability and diversity in where design ideas come from but also for oversight and accountability on the design/implementation choices made by each devloper.




---

**Question**

How do the themes of _Growing a Language_ relate to the lab we did this week?

**Response**

The Growing a Language essay was extremely relevant to the revamped cs5 lab we did in class this week. "A primitive is a word for which we can take it for granted that we all know what it means. For this talk, I chose to take as my primitives all the words of one syllable, and no more." [Steele, 1998] In Growing a Language the primatives were one syllable words. In the fluency lab, the primitives were these functions that were used to reverse, change volume etc. of sound clips. In growing a language Steele was able to "define" new words either word by word or by using a rule because the primitives that he started with were good tools to start with. In class, we rapidly identified a problem with the primitives in the cs5: they did not work well to define new words. The Growing a Language talk showed us how important it was to have a language that can grow and serve new purposes that the designer did not necessarily intend (or at least did not imagine) but the cs5 primitives did not allow for a user to do anything that was not built explicitly into the language. In the fluency lab we were tasked with making the cs5 primitives more similar to the one-syllable-english used by Steele in Growing a Language. If we could only make it so the primitives could be composed in order to serve new purposes, or allow a user to do a modify, save, or play action without doing them all at once then we would have updated the grammar to a point where a user could now use our primatives to define new words,rules and uses. This made us think of the rule set out for us in Bloch: "You can’t reasonably hope to imagine everything that everyone will do with an API, or how it will interact with every other part of a system." [Bloch,2006] In order to define a good API (or language) its necessary to realize that wont have thought of everything that a user will want to do so its vital that you write your grammar in such a way that new uses that you have not imagined can be incorporated.


---

**Question**

How would you know a well-designed language? What are the symptoms? How would
you know a poorly designed language? What are the symptoms?

**Response**

Language design is tricky, and it's hard to get it right. Determining which
languages are good is important to know which ones to use --- even a DSL that is
designed exactly for your purpose is not a good choice if it is poorly designed.
Steele would say, and we would agree, that a good general purpose language is
not necessarily marked by how good its syntax is or how many features it has but
rather by its ability to grow.  No language can cover all use cases, and if
there's a different syntax between built in types and user defined ones, overall
awkwardness results. Steele believes that good languages are, in fact, small at
their core and are easily extensible so users can define the features they
need. Adam doesn't necessarily agree with this because it's nice to have
standardized common features, although does agree that these should be part of
standard libraries and not the language core.

Domain-specific languages, on the other hand, have much less necessity to grow.
Growing a domain-specific language would probably mean that it is being used
outside its domain, so growth is not a priority. Being able to grow doesn't
make it a bad language, but it's not as necessary as it is for general purpose
languages.

Robin believes that good documentation is necessary for a good language because
you need to be able to actually use a language for it to be good. Adam
disagrees because he believes that the goodness of a language is basically
independent of its documentation, although he agrees that documentation is good
for everyone involved.

The principle of least astonishment is also important in good languages. This
is true in the traditional "if I type something that's valid, it should do what
I typed," but also in a fail fast principle. Usually not every string is a
program in a language, and a programming language is more useful the faster it
tells you about invalid programs. So if you've done a small amount of testing
of a program, having it fail due to something like a syntax error when an edge
case is hit is pretty surprising and should be avoided if possible.

---
 

In what way is an API a language? 

**Response**

An API is somewhat of a precursor to a language: once an API gets complicated
enough, we can start to think of it as an internal DSL, and it may eventually
become its own language. A good example of this is the graphics library QT. QT
started as just a graphics library where you could draw things, but now it has
such a heavy preprocessor that it tacks on before sending it to the C++
compiler that it is essentially a language of its own. But even when an API is
just an API, it is still shares a lot with a language. Both are used by people
other than those who wrote it, and can be used to do things that the designers
did not even imagine. Both an API and a language are used as a human interface
to a system: in a general purpose language, this system is the computer as a
whole, but in an API it is just the one application.

There are, however, some differences. A full-blown programming language usually has a lot
more nouns than an API does, since the nouns that the API has are usually
implicit to the application. As an example, an "API" for a light bulb might
have the `turn_on` and `turn_off` functions, while the equivalent in a GPL
would be to have the light bulb noun as a separate noun.

Overall, we would say that an API is a very basic DSL and thus shares some
features of languages while being different in other aspects.

---

**Question**

The comments on the Pavlus article seem to set up a conflict between
professional programmers and everyone else. What is the essence of this
conflict? Do you sympathize more with the substance of the article's arguments
or with the substance of the majority of the commenters' arguments? Do you
sympathize more with the tenor of the article or the tenor of the majority of
the commenters?

**Response**

The essence of the conflict between professional programmers and everyone is
that the professional programmers have seen many bad attempts at making coding
"easier" and are fearful of being forced to use another. In the attempt to make
programming easier, languages such as Scratch have been developed, where it's
fairly easy to do atomic tasks that the developers thought of, but are, as
Steele would put it, unable to grow. So many bad attempts have been made, ones
that just cater to new users but are painfully hard to do anything advanced in,
that the professional programmers have become wary of the attempts. In short,
the programmers are afraid of oversimplification so much that they support no
simplification at all.

While the fear of oversimplification may not be entirely rational, there are
dangers with the movement of programming languages closer to natural languages.
Natural languages are almost inherently ambiguous and in class most people
agreed that programming languages should be unambiguous. Thus, to use a natural
language as a programming language, somewhat arbitrary decisions must be made
to remove the ambiguity, which can make it harder to write because one must
know about these decisions to program correctly.

On the other hand, simplification of programming languages is a worthwhile task
and is certainly _possible_ to do without oversimplifying them. Professional
programmers should not immediately dismiss attempts at simplification since if
attempting is discouraged, no progress will be made.

What's interesting, though, is that programming languages are already not all
that difficult to learn: as commenter Peter says, "In particular, you can learn
C++, say, much more easily than you can a new natural language." Sure, there are
many rabbit-holds that can lead you to years of studying a language, and some
communities are not particularly welcoming to newcomers, but programming
languages _were_ designed for people to be able to use and are still relatively
good at that.

---

**Question**

How do implementation choices (e.g., as an interpreter/compiler or as an
internal DSL) affect the user experience? Can or should we always hide our
implementation choices from users?

**Response**

Programming languages are the interface between human and computer, so they
should be designed to be easily understood by both parties. Generally, it's
simple for language designers to cater to the computer since computers are
relatively simple and programmers deal with computers a lot. Making a language
that is good for humans, however, is much harder, so language designers
constantly need to think about what is best for them. One goal of a language is
to take a relatively complex object and make it easy for humans to interact
with. Often, this means that there are some things that one could do directly
in the domain that will become impossible if using a language. Language
designers must make implementation choices to decide which things in the domain
should be carried through and which should become impossible. For example, if a
designer decides that a language should be interpreted, it becomes impossible
to write a program in that language that is to be compiled. This sort of design
choice affects users a lot because it restricts what they can do, and these
choices cannot be hidden from users because they are fundamental to the
language. Another concrete example is in something like the C++ standard
library, where the `set` class is supposed to be a generic set but was
implemented as a tree, and they later had to add an `unordered_set` class for
people that wanted a hashset instead.

While these design choices do change how a person uses the language, the
overall user experience can be overall good with many different choices. Often
making the design choices very clear to the users helps with understanding,
since the principle of least surprise can be upheld much more easily.

---

**Question**

The Pavlus article mentions the researchers' comments that people preferred
"natural-language replacements for some of the more abstruse syntax". In other 
words, people found it easier to work with code that looks more like a human language (e.g.,
English). Consider the following quote by William R. Cook, one of the creators
of JavaScript:


> The experiment in designing a language that resembled natural languages (English
> and Japanese) was not successful. It was assumed that scripts should be
> presented in “natural language” so that average people could read and write
> them. … In the end the syntactic variations and flexibility did more to confuse
> programmers than to help them out. It is not clear whether it is easier for
> novice users to work with a scripting language that resembles natural language,
> with all its special cases and idiosyncrasies. The main problem is that
> AppleScript only appears to be a natural language: in fact, it is an artificial
> language, like any other programming language. … even small changes to the
> script may introduce subtle syntactic errors that baffle users. It is easy to
> read AppleScript, but quite hard to write it.
[[Cook 2007, page 1-20]](https://dl.acm.org/citation.cfm?doid=1238844.1238845)

Are these two experiences of natural languages at odds with one another? Would
you choose to include natural language in the design of a DSL? If so, how might
you do so? If not, why not?

**Response**

This is an extremely interesting question and debate that we think will be a major talking point in CS over the next years. There will always be a core of people that are loyal to the "original" type of programming languages, but in order to evolve the designers of programming languages will try to appeal to a broader audience by trying to making PLs more like natural languages. We decided that these two experiences are not at odds with each other but there are important truths to both experiences. The Pavlus article we think was clearly written by someone that wasn't well-educated enough about the issue to have his own unique insights but that is not at all to discount the article because the fact of the matter is that __analysis of programming languages will not always be done by people that are experts in computer science.__ The points brought up about perl and Randomo are funny and interesting and it _is_ a problem that novices can't read/write C-based code at all intuitively but also the problem raised by Cook is a serious one. __Programming languages should not masquerade as natural languages unless they truly are one.__ The principle of least surprise would tell us that if something looks like a natural language then it should _behave_ like a natural language. Each natural language has slang, mispronunciations, and differences in use that are not acceptable in PLs because computers do not (yet) have the same kind of flexibility of interpretation that humans do (computers can not see your body language, guess as to your intent, etc.) In class we decided that PLs should be deterministic and unambiguous but natural languages are neither of those things which makes raises a question of how much like natural languages we want our PLs to be.

We did decide, however, that some parts of natural languages are important to incorporate into a DSL that we were writing. Consider python's looping syntax vs. Java's
for i in range(n):             vs.         for (int i=0; i<n; i++){
   foo(i)                                     foo(i);
   bar+=1                                     bar++;
                                           }
These loops do the same thing but the python is far more readable to someone that does is unfamiliar with code. We think that it is good to incorporate nouns and certain concepts from natural languages into a PL but it is vital that it is super clear that PLs are a 'different beast' than natural languages. We want languages that are easy to write (both for experienced and inexperienced programmers) and easy to read for everyone but we also __need__ languages that give us what we want and expect from a programming language.
---

**Question**

Briefly describe how you split up the work for this assignment.

**Response**

We did the readings separately and then met on friday to generate outlines for all the questions and discuss our opinion on the articles. We discussed and wrote outlines and then split up the writing/cleaning up of our ideas to do on our own time. 
Robin did:Natural language/JS quote
Adam did: How do implementation choices effect the UI, Comments one, How is an API a language, Good language vs. bad language


---
