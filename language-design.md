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
> and back what they sell. [Steele, 1998]

We both agree with this quote for the most part, but we are a bit concerned that sometimes maintainers would disappear. If languages lean slightly cathedral from a shopping mall model, then they can have patterns for dealing with this problem. Real-life shopping malls kick vendors out if they stop paying rent, but this doesn't work when "Public APIs, like diamonds, are forever" [Bloch, 2006].

> A small programming language might take but a short time to learn. 
> A large programming language may take a long, long time to learn, 
> but then it is less hard to use, for we then have a lot of words at hand [Steele, 1998]

We both agree with this in general, though it is possible to construct the syntax in a way
that would make the language either easier or more difficult to learn regardless of size.
In Python, the language is small, but there is a large library, so there are ways to have
"a lot of words at hand" without making a larger language. Perl has complex syntax and 
semantics [[Kegler, 2008](http://www.jeffreykegler.com/Home/perl-and-undecidability)], making it a large language, and as stated in the Pavlus article novice programmers certainly found the language to be difficult [Pavlus, 2012].

> In an informal design the specification is usually in some form of natural language, 
> probably including a set of illustrative DSL programs. A formal design consists of a 
> specification written using one of the available semantic definition methods...Clearly, 
> an informal approach is likely to be easiest for most people. [Mernik _et al_., 2005]

While informal specification is easier to specify, there are many tools for formal specification
that makes parsing the language easier, therefore having a formal specification makes 
the language construction easier overall. In Daniel's experience, almost every DSL that
isn't built into the host language uses a formal syntax definition, even if the semantics
are informal. For example, the [sudoers(5) man page](http://www.sudo.ws/man/1.8.14/sudoers.man.html)
even includes the BNF for a sudoers file.

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

A well-designed language is extendible, has a relatively small core vocabulary, is easy to learn (though not necessarily for everyone),
is easy for the user to read and write, and has good documentation.
On the other hand, a poorly designed language makes it difficult to write libraries and extentions,
has inconsistent libraries, has a large and cumbersome core vocabulary, has a steep learning curve,
or is otherwise difficult to use.
These lists are general statements, of course, not universal; a well-designed language
need not have all the elements in the first list, and a poorly designed language need not have
any of the elements in the second list.

---
 

In what way is an API a language? 

**Response**

APIs differ from DSLs in that APIs don't implement their own syntax, and instead borrow it
from the host language, however they still have vocabulary and grammar. You still must use 
the vocabulary of the API in the way that it allows.

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

Implementing an internal DSL will give it the feeling of the host language, allowing more
familiarity with the syntax, but it won't give the developers as much control over what the
users can do. 
The choice of interpreter versus compiler will affect the build process, or whether a user
has to compile before running a program.

In general, we can't always hide our implementation choices. Obviously, whether you must
compile or not should be known by the user.
When it is possible to hide our implementation choices, it makes it easier to change them
later on without changing the user's experience, so choices like using an interpreter or a 
compiler should be made carefully as they are probably going to be permanent.

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

Not necessarily; Quorum is more structured than AppleScript, so it's possible to include
natural language, and thus make the language more understandable to novice users, as long
as the language is structured enough for the user to parse it as proper code. Where AppleScript
fails is in making the syntax too similar to English, but the actual parsing doesn't support
syntax that would be acceptable in English, and may be written by the users,
but isn't handled by the language.
Quorum is structured enough for its users to understand that their code must be structured,
so while it's easier for them to understand there is less of a chance they will make syntax errors.

Whether or not to use natural language depends on many factors, such as the purpose of the language and who its users will be, and 
what parsing libraries are available for natural language syntax. For example, 
"Quorum... started as an interpreted language originally designed to be 
easier to hear through screen readers for blind or visually impaired users" [Stefik _et al_., 2014](http://quorumlanguage.com/about.php),
so using natural language was important as it would be easier to hear.
Neither of us are particularly opposed to using natural language in a DLS's design, 
though having syntax that is heavily structured makes it less likely that users will try
to import messy syntax from a natural language and make errors in their code.

---

**Question**

Briefly describe how you split up the work for this assignment.

**Response**

Daniel was the driver for half the time, and Anna was the driver for the other half.
We did the readings individually, then discussed and answered the questions together. 
Each commit was made by the driver for the relevant changes.

---
