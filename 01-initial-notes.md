# Initial project notes

The project idea is to find out whether we can use the spreadsheet metaphor for programming 
agent-based models (ABMs). We want to use HCI methodology for the system design, i.e., start
by understanding how spreadsheet users think about the problem, how would they try to use
existing spreadsheet systems for the problem and what needs to be added to those systems to
make this possible.

## Methodology

For HCI methodologies, the online [Encyclopedia of Human-Computer Interaction](https://www.interaction-design.org/literature/book/the-encyclopedia-of-human-computer-interaction-2nd-ed)
is a great resource - it is very long and covers everything, but it may be useful to look at
a chapter or two from here.

For our project, we need to start with some kind of exploratory user study - talk to spreadsheet 
users and see how they would approach the problem. This would likely take some form of semi-structured
qualitative study. See [Semi-structured qualitative studies](https://www.interaction-design.org/literature/book/the-encyclopedia-of-human-computer-interaction-2nd-ed/semi-structured-qualitative-studies) 
in the encyclopedia (this is also very long, so I would not read every single section, but it 
gives good overview).

At a later stage (when we have a system), it may make sense to do quantitative evaluation
(to evaluate how well people can use the resulting system). The methodology for this would be
covered in [Experimental Methods in Human-Computer Interaction ](https://www.interaction-design.org/literature/book/the-encyclopedia-of-human-computer-interaction-2nd-ed/experimental-methods-in-human-computer-interaction).

## Inspirations

What we are trying to do is to use human-computer interaction methods for programming systems
research. In academic world, this kinds of work tends to get published in [UIST](https://dblp.org/db/conf/uist/index.html)
and [CHI](https://dblp.org/db/conf/chi/index.html) conferences - but those are general HCI conferences
and have lots of publications about things that are not programming-related. [VL/HCC](https://dblp.org/db/conf/vl/index.html)
is another source of possibly more relevant materials.

I have a couple of papers that I'm aware of that are interesting and somewhat in the general related area
(again, this is a lot of material - we do not need to read all of those now!) but it may be useful to skim-read
some to get some idea about the methodologies (that is what we need to figure out first).

* [1] [Varv: Reprogrammable Interactive Software as a Declarative Data Structure](https://vis.csail.mit.edu/pubs/varv/)
* [2] [Idyll: A Markup Language for Authoring and Publishing Interactive Articles on the Web](https://idl.cs.washington.edu/files/2018-Idyll-UIST.pdf)
* [3] [Living Papers: A Language Toolkit for Augmented Scholarly Communication](https://idl.uw.edu/papers/living-papers)
* [4] [reCode: A Lightweight Find-and-Replace Interaction in the IDE for Transforming Code by Example](https://www.cs.cmu.edu/~woden/assets/uist-21-recode.pdf)

[1] introduces a new kind of programming system. This paper does not follow the typical (1) exploratory study, (2) design and implementation, (3) evaluation
pattern - it has a more high-level design goals that the authors argue for without a particular empirical study. The evaluation is via case studies in section 5.

[2] is perhaps more relevant example - it documents the design space for document authoring systems (figure 2) and identifies a gap - it then identifies
a set of requirements (using author's expertise in the domain) - the initial design is then assessed via interviews with domain experts (this is a nice thing to do!)
and evaluation is via a range of examples.

[3] uses iterative design methodology - the authors use the tool, discuss it with a large number of colleagues and iteratively develop and design it
(but there is no initial study to figure out what the design should be - it is again based more on experience of the authors)

[4] uses "Formative Interviews" which is perhaps closer to what we need to do for ABMs in spreadsheets - they use interviews to figure out what 
kind of tools are programmers currently lacking (This is "needfinding" and Google finds [various resources about it](https://www.google.com/search?q=needfinding+hci)).
The interviews are with just 7 people  and are used to identify three design goals. (The paper then describes system based on those 
design goals and evaluates it through empirical study.)
