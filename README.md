# Presentation schedule

* Talks the week of FIXME during lecture or recitation.

* Link to presentation on YouTube due on FIXME

* Signups

# Choosing a topic

Successful programming languages tend to evolve over time, especially
in the context of their community. Some languages use standards
committees to represent this community; others use more informal
processes. Either way, any potential evolution is frequently
encapsulated into a change proposal, which the community can evaluate,
discuss, and further enhance. Frequently the change proposal is
rejected outright, but sometimes it may live on in some other way, or
even influence another language.

Once you have picked a language to study -- Java, JavaScript, Python,
or Scala -- find a reasonably substantial change proposal for that
language and choose that as your presentation topic. This change
proposal may be currently in a proposed state, or it may now be
rejected, accepted, or implemented. You may find it most
straightforward to write about accepted proposals that are now
implemented. However, rejected proposals may be of especial interest
if the language later returned to that proposed idea, but in some
other way.

Change proposals will be in the form of a PEP, SIP, JEP, JSR, or
similar document. You may want consider subsequent proposals that cite
the proposal as part of the development of your theme. See below for
resources.

And then what? You need to carefully consider the change proposal in
terms of documenting its proposed impact to the language and its use.

# Creating your presentation

Your team's presentation on this change proposal should exhibit the following
characteristics:

* Apply the terminology and concepts we have used throughout the
  course. If language feature Baz supports higher-order functions, and
  takes advantage of nested scopes and currying, state so in such
  terms and concepts. If feature Bar provides syntax that makes
  certain common tasks easier or less error prone in the language,
  perhaps describe the syntax in the context of allowed grammar
  productions.

* Provide supporting code examples, diagrams, and other evidence. Such
  examples can be original to you or can come from the change proposal
  and any corresponding discussion.

* Cite supporting evidence using primarily primary sources from the
  community of the language being investigated.

* As usual, academic standards of plagiarism and attribution do apply.

When citing evidence, you should look for authority over form. For
your presentation, blog posts and their comments, emails in mailing
lists, and Q&A in StackOverflow-type sites are valid primary sources,
even if informal, along with articles and books. What matters here is
the content of the discussion and where it went. Consider carefully
the author of the source, and its centrality, in the conversation. In
addition, do filter out noise and irrelevance. Careful selection and
presentation are important parts of what we will evaluate.

Presentations must be written in [Markdown][], specifically using the [GitHub
dialect][]. However, you are allowed to embed Latex for mathematical
notation, as you see fit, using the following convention from Pandoc:
`$ <latex goes here> $`. (GitHub used to render such notation with
MathJax, and it's a major missing feature for us at this time.)

Use Markdown fences to demarcate code examples. Select the proper
language (`java`, `javascript`, `python`, `scala`):

    ````python
    def f(x):
        return x * 2
    ````

Under no circumstances should you embed code samples in your
presentation **as an image**! (This admonition is based on previous
experience. But seriously it's so much easier to do it the right
way...)

Use backticks (`` ` ``) to quote a short code fragment. So for example,
here's the code fragment to show making a call to the above function:
`f(42)`, which can be written like so inline `` `f(42)` ``.
	
Introduce long quotes with `>`. Use endnote style links: use
`[text][optional-id-if-different]` in the text, followed by an endnote
with corresponding link at the end.

More on using Markdown in your presentation can be found at
this useful [Markdown cheatsheet][].

# Presentation

Distill your inquiry into your topic to something to present to the
class in a five minute slot:

* 20 unique slides, spaced *exactly* 15 seconds apart, for a total of
  5 minutes. The Adobe PDF viewer can perform this autoplay, and we
  be using this feature in clas.

* This is a class about programming languages, so do show and talk
  about code! You want to find a good balance between describing a
  concept abstractly and demonstrating specific code usage in the
  language you're discussing.

* Slides must be written in Markdown, however, they can embed other
  media or use embedded Latex, much like the lecture notes do.

* Presentation is a PDF file generated via Beamer and pandoc; see the
  below section.

* Everyone on the team must be part of the presentation. Talk to an
  instructor if this is a problem.

The style we are requiring for this presentation is actually closest
to the Ignite format, vs a typical conference lightning talk. I
recommend this [blog post][presenting-for-ignite] as a good start: it
walks you through the process of going from a storyboard to a finished
product. You may also find that a short presentation can sometimes
require more work than a longer presentation: that's the essence of
getting your content distilled down.

# YouTube version

Once you have practiced and gotten feedback on your presentation in
front of the class, it's time to produce a video for upload to
YouTube. This can be a simple screencast where you are narrating your
slides; or you can also have video of the presenters. It's up to
you. The important thing: all YouTube presentations must have good
audio and nonshaky video. Slides must be clearly visible. And again,
you will do this with an auto advance every 15 seconds.

# Generating your presentation slides

Your presentation must be convertable to PDF by using the pandoc
tool. You will use the same pipeline as I have used in generating
lecture notes. Running

````bash
$ ./generate talk.md
````

will produce `talk.pdf`.

# Installing `pandoc` on Ubuntu

It's simple on Ubuntu, as might be expected:

````bash	
$ sudo apt-get install pandoc
$ sudo apt-get install latex-beamer
````

# Installing `pandoc` on OS X

For OS X, download and install the following packages:

1. pandoc DMG at https://code.google.com/p/pandoc/downloads/
2. BasicTex at http://www.tug.org/mactex/morepackages.html
3. MacTeX-Additions also at http://www.tug.org/mactex/morepackages.html

Then do the following:

````bash
$ sudo tlmgr install pgf
$ sudo tlmgr install pgf-umlsd
$ sudo tlmgr install xstring
$ sudo tlmgr install smartdiagram
````

# Help for `generate`

````bash
$ ./generate  --help
usage: generate [-h] [--format FORMAT] [--incremental] source

Simple driver for pandoc. Or use pandoc directly for more options.

positional arguments:
  source             Source markdown file

optional arguments:
  -h, --help         show this help message and exit
  --format FORMAT    Output format
  --incremental, -i  Incremental display of lists
````

# Resources and parting words

Here is a sample resource in where you should start in your investigation:

* Python uses [PEPs][] (Python Enhancement Proposals) for language
  proposals. Two mailing lists are typically used, [python-ideas][]
  and [python-dev][] to discuss PEPs and their implementation. In
  addition, you may find the "What's new in Python x.y" useful in
  understanding the scope of changes; you may want to look at series
  of these "What's new" summations.

The other languages will have similar places to look.

Lastly:

* Be creative.
* Remember to have fun with your topic!

<!-- references -->

[GitHub dialect]: https://help.github.com/articles/github-flavored-markdown
[Markdown]: http://daringfireball.net/projects/markdown/
[Markdown cheatsheet]: https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet
[PEPs]: http://www.python.org/dev/peps/
[presenting-for-ignite]: http://www.speakingaboutpresenting.com/content/fast-ignite-presentation/
[python-dev]: http://mail.python.org/mailman/listinfo/python-dev
[python-ideas]: http://mail.python.org/mailman/listinfo/python-ideas
