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
   "As mentioned inj section 1.1, a quantitative..."
   1. Doing whats comfortable often leads to not doing what is hard (which potentially deters from building a language even if that language would be more comfortable in the long run)
   2. Designing a DSL is not even that hard, but takes mental effort to decide that you need to do it, and then more mental effort to decide to actually do it. unfamiliar choice, so defaults to not doing it
   3. Difficult to look past "short-term considerations" (getting code written) in order to see potential long term benefit
   4. Good policy for life...don't postpone hard things because eventually postponing just means not doing

# Quote 2, Bloch 2006
   "If its hard to find good names, go back..."
   1. A good idea for an API, when someone else will be using it
   2. Questionable advice for programming large scale, modular projects. what about helper functions? serve specifc and important purpose, but not necessarily obvious names "helper_function_one()"
   3. Think about binary tree traversal, simple concept but requires helper functions to do several, easy, recursive tasks. those functions dont have obvious names

# Quote 3, Steele, 1998
   "But the key point of the bazaar is not that you can..."
   1. helping with design is sometimes more important than helping with building
   2. a little bit weird b/c if a target for a project keeps changing then wont have a clear focus
   3. reference quote about adding complex numbers, rational numbers, intervals, game, vector as primitives. he comes to the conclusion that "no. definitely not." which seems to contradict this part of the paper. why should the chief designers let random people have lots of power in the design process? in order to have a strong language you need to have a strong vision that cannot be watered down by many different people that all have different goals and use cases
   4. people should be able to add to "their own language" aka write libraries, define first class objects through classes etc.




---

**Question**

How do the themes of _Growing a Language_ relate to the lab we did this week?

**Response**

1. point of the lab to notice that the end goal of the cs5 lab kind of sucked because all it did was create primatives that were unable to work together
2. GaL had the whole point of starting from primatives and then building upwards because all of the primitives were able to be expanded upon
3. what we wanted to do in the lab was recreate the cs5 primitives so they could serve the same purpose that the one syllable english words served Steele. We could add rules that gave new meaning to the primitives, we could chain the primitives together into sentences that had larger meaning
4. the vocabulary of the cs5 lab was completely broken because all the words could only be used alone, in order to create a language you need to be able to use words together so we have to change the way the primitives work


---

**Question**

How would you know a well-designed language? What are the symptoms? How would
you know a poorly designed language? What are the symptoms?

**Response**
   1. a good general purpose language is not necessarily marked by a perfect grammar or syntax, but instead by the ease of growth
   2. a good DSL however, we believe, should be almost perfect when released. there is room for improvement from the developers standpoint but in order for it to remain a crisp DSL its important that there arent "too many cooks in the kitchen" designing the language.
   3. "APIs should be easy to use and hard to misuse..." bloch tip #6
   4. all good languages should have good documentation - Robin
   5. good languages can have objective merits even with bad doc. Good languages and good documentation are independent of each other - Adam
   6. Good languages operate under principle of least astonishment, bad languages are astonishing
   7. bad languages are cluttered with too many primitives, rules
   8. bad languages dont have the ability to grow
   9. bad languages take a while to let you know that theyve failed, better to fail at compile time than run time


---
 

In what way is an API a language? 

**Response**

1. it is used by people other than those that wrote it
2. API basically just internal DSL, interface to a system
3. System needs to be controlled, need a language to control the system, use the API to control the system, thus the API is a language
4. not that many nouns! mostly verbs that use the nouns inherent to the host language
5. have documentation
6. means for programmer to talk to a computer
7. user should be able to use API to do things that designers did not imagine, otherwise just a series of buttons which is a pretty lame API


---

**Question**

The comments on the Pavlus article seem to set up a conflict between
professional programmers and everyone else. What is the essence of this
conflict? Do you sympathize more with the substance of the article's arguments
or with the substance of the majority of the commenters' arguments? Do you
sympathize more with the tenor of the article or the tenor of the majority of
the commenters?

**Response**

   1. programmers afraid of oversimplification
   2. dangers of moving PLs closer to natural language is that PLs do not function like natural languages. you can make syntax erros and use nouns/vers that arent quite right in natural language and still get the meaning across but in PLs a computer either a) wont do anything (error) or b) will do something that you didnt want it to do
   3. there is a lot of "meanness" on CS forums, people often want to seem smart and feel smart and dont want their field to be corrupted by "bad programmers"
   4. community should want to include everyone but doesnt work that way right now
   5. defintiely are problems with natural language like PLs in that they dont work that well but programmers should be trying to find a solution for that problem in order to expand and progress their field, not just criticizing the attempts being made
   6. bad solution worse than no solution, but people so afraid of bad solutions that they wont help to find a good solution. sympathize with both parties (on one hand you dont want bad languages creating bad programs written by bad people, but on the other hand the more people that have the ability to write programs the better the tech sphere will be)
   7. "in particular you can learn C++, say, much more easily than you can a new natural language" <-- good quote


---

**Question**

How do implementation choices (e.g., as an interpreter/compiler or as an
internal DSL) affect the user experience? Can or should we always hide our
implementation choices from users?

**Response**

   1. made a few APIs, try to bring through all the important subtleties of the underlying model when desgining API in order to avoid oversimplification
   2. important to balance simplification/increased ease of use (a partial purpose of the API) with faithfulness to the underlying system
   3. if there is a design choice made that could go one way or the other, a designer should make clear that choice so that the user can make an informed choice about how to use the language
   4. implementation choices effect how the user writes it but not necessarily the "overall user experience" (rate your experience on a scale of 1-10) may not be affected by many implementation choices, instead by the overall design of the language

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

   1. not at odds with each other...consider python: "for i in range" is way more natural language than "(int i =0; i <n; i++)" but maintains all the expressiveness
   2. resonates with us that PLs should not masquerade as natural languages if they are not natural languages. each natural language has slang, mispronunciations, differences in use, that are not allowed in PLs
   3. in class we decided that PLs should be deterministic/unambiguous but NLs are not deterministics or unambiguous. 
   4. Good to adopt words and concepts from natural languges because it makes it easier for those who have not before written code to get started but its important to make it clear that PLs are a different animal in that they have a more strict syntax. At least until we teach computers english
   5. In a design of a DSL we think it would be good to try and adopt nouns and certain concepts (for i in range) from natural languages but its also crucial for the usability that its clear _how_ to use the language and natural languages dont necessarily give that clarity

---

**Question**

Briefly describe how you split up the work for this assignment.

**Response**

We did the readings separately and then met on friday to generate outlines for all the questions and discuss our opinion on the articles. We discussed and wrote outlines and then split up the writing/cleaning up of our ideas to do on our own time. 
Robin did: Quotes, Themes of growing a language, Natural language/JS quote,
Adam did: How do implementation choices effect the UI, Comments one, How is an API a language, Good language vs. bad language


---
