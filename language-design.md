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

> We should not make the Java programming language a cathedral, but a plain
> bazaar might be too loose. What we need is more like a shopping mall, where there are
> not quite as many choices but most of the goods are well designed and sellers stand up
> and back what they sell." [Steele, 1998]

We both agree with this quote for the most part, but we are a bit concerned that sometimes maintainers would disappear. If languages lean slightly cathedral from a shopping mall model, then they can have patterns for dealing with this problem. Real-life shopping malls kick vendors out if they stop paying rent, but this doesn't work when "Public APIs, like diamonds, are forever" [Bloch, 2006].

> 

---

**Question**

How do the themes of _Growing a Language_ relate to the lab we did this week?

**Response**

One of the main themes of _Growing a Language_ is summarized by the quote at the bottom of page 12, "A good programmer builds a working vocabulary. In other words, a good programmer
does language design, though not from scratch, but by building on the frame of a base
language." [Steele, 1998]. This is what we did with our lab assignments, by building vocabulary for people to manipulate PCM audio. This was not just building vocabulary for use in the Python programming language, but also building vocabulary for use _with the rest of the library_. The original design of the lab assignment did not allow chaining multiple pieces of the vocabulary together, so any function needed to be a part of the library from the beginning (a cathedral-style design). We re-designed the library to allow the functions to be combined with each other, allowing a more bazaar-like approach. This is a better library design because "in the bazaar style of building a program or designing
a language or what you will, the plan can change in real time to meet the needs of those
who work on it and use it." [Steele, 1998].

---

**Question**

How would you know a well-designed language? What are the symptoms? How would
you know a poorly designed language? What are the symptoms?

**Response**



---
 

In what way is an API a language? 

**Response**



---

**Question**

The comments on the Pavlus article seem to set up a conflict between
professional programmers and everyone else. What is the essence of this
conflict? Do you sympathize more with the substance of the article's arguments
or with the substance of the majority of the commenters' arguments? Do you
sympathize more with the tenor of the article or the tenor of the majority of
the commenters?

**Response**

The essence of the conflict is that tools which are easy-to-use for novices might not be the best tools for experts. Many of the commenters would trade program readability for efficiency (usually programming speed or runtime speed). [[Unclemilford, 2012](https://www.fastcodesign.com/1665735/why-arent-computer-programming-languages-designed-better#comment-f7558800-41fb-11e1-921b-9794fc737ae8); [STRENGTHINESS, 2015](https://www.fastcodesign.com/1665735/why-arent-computer-programming-languages-designed-better#comment-93e75ca0-9b5b-11e4-a3e4-4930d33952b2)].

We both think that both the article and the comments raise some good points. The article asks "Why shouldn’t [programming languages] be humanely designed?" [Pavlus, 2012], and strongly implies that the answer is "they should".
However, it makes the implicit assumption that it should be humanely designed for "novice programmers". The comments point out that the needs of novice programmers aren't the needs of professional programmers, but also downplay the importance of usability to those professional programmers (for example, see [STRENGTHINESS, 2015](https://www.fastcodesign.com/1665735/why-arent-computer-programming-languages-designed-better#comment-93e75ca0-9b5b-11e4-a3e4-4930d33952b2)]). We feel like usability is still important to professional programmers, but that the methods for making programming languages usable for this specific group are different from the ones for the general public.

The premise of the article is flawed on a few levels, but given the flawed premises the article is good at explaining its points well. The commenters, being multiple people, vary widely in understandability and tone, but are generally not as good as the article.


---

**Question**

How do implementation choices (e.g., as an interpreter/compiler or as an
internal DSL) affect the user experience? Can or should we always hide our
implementation choices from users?

**Response**



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



---

**Question**

Briefly describe how you split up the work for this assignment.

**Response**



---
