## Free and Open Source Software
### An Introduction

**Lallu Anthoor**

_Senior Developer, SAP Labs India Pvt. Ltd._

_`lallu[dot]anthoor[at]pm[dot]me`_

<br>

`https://bit.ly/fossstm`

---

### Agenda

- What is FOSS?
- Why FOSS is important?
- Why should you be part of FOSS?
- How you can be part of FOSS?
- Demo

---

### What is FOSS?
- "free" as in "free speech", not as in "free lunch"
- you are free to use the software for any purpose
- you are allowed access to the source code
- works based on the 4 pillars of freedom

Note:
The "free" in FOSS is all about freedom. Not about money. Having not to pay for the software
is only a side effect of having the freedom to use the software. The "free" should be compared
to the free in free speech. Not to the free in free lunch. The fundamental priciple that guide
a FOSS project is the respect for the freedom of the people to not just use it, but also to
see and understand how it works and also modify it to suit their needs.

The "open source" means that the source code for the software is openly available for everyone
to access. You are allowed, and even encouraged, to make changes to the source code to make the
software better.

The free software movement is lead by Free Software Foundation (FSF).It was founded by Richard Stallman,
known for GNU, gcc, etc., in 1985. Since then the FSF plays a pivotal role in guiding the FOSS
community and to point out the pitfalls and dangers of using proprietary software. The FSF has
laid out 4 pillars of freedom which all FOSS projects must uphold.

------

#### 4 pillars of freedom
- The freedom to run the program as you wish, for any purpose (freedom 0).
- The freedom to study how the program works, and change it so it does your computing as you wish (freedom 1). Access to the source code is a precondition for this.
- The freedom to redistribute copies so you can help others (freedom 2).
- The freedom to distribute copies of your modified versions to others (freedom 3). By doing this you can give the whole community a chance to benefit from your changes. Access to the source code is a precondition for this.

Note:
The four pillars of freedom are numbered 0 to 3. Somewhat similar to the laws of themodynamics.
The freedoms 1-3 were already known by 1990s. But then FSF realised that the freedom to run the
software need to be explicitly mentioned. Since it was more basic than the other 3, it was named
freedom 0. This also goes hand in hand with how arrays are indexed, or in general, how counting
is carried out in computer world.

Freedom 0 grants to you the rights to run the program however you wish for whatever purpose. It
is not bound by any restrictive EULAs. Freedom 1 allows you to study the inner workings of a
program. Which means implicitly that you have access to the source code of the program. You are
also allowed to make changes to the source code and tailor the program to work in a manner suited
for your needs. Freedom 2 gives you the right to freely distribute the software. This is explicitly
prohibited by the proprietary software, and is considered software piracy when you violate this.
Freedom 3 gives you the right to freely distribute the modified version of the software that you
created, without any legal obligations to the original software. When distributing the modified
version of the software, depending on the license one of two things are possible. If the license is
permissive, you are allowed to even sell your modified version of the program for profit. If the
license is restrictive, you will be forced to make your modified software also open source.

------

#### Who builds FOSS?
- source code is publicly available
- anyone can contribute
- driven by community
- moderated by maintainers

Note:
Open source projects are initially developed in two ways. First one is when a big company like
Google, Microsoft, Netflix, LinkedIn or SAP builds a software internally, and later makes the
source code openly available. This is what happened with projects like [kubernetes](https://github.com/kubernetes/kubernetes) (Google),
[Visual Studio Code](https://github.com/microsoft/vscode) (Microsoft), [Chaos Monkey](https://github.com/netflix/chaosmonkey) (Netflix), 
[Kafka](https://github.com/apache/kafka) (LinkedIn) and [OpenUI5](https://github.com/sap/openui5) (SAP). The
second way is when a person or a group of people come toghether to realise an idea and decide
to make it available as open source library. For example, [hugo](https://github.com/gohugoio/hugo) and [cobra](https://github.com/spf13/cobra) developed by Steve Francia,
[Linux kernel](https://github.com/torvalds/linux) developed by Linux Torvalds, or [ANTLR](https://github.com/antlr/antlr4) by Terence Parr.

Irrespective of whether they are started by a small group of individuals or a giant organization,
once the source code is made public, everyone contributes to it. These contributions are done
voluntarily by people in their free time or time dedicated for open source contributions in their
work schedule.

Usually, a strong community is built around each of these software to support the main creators.
There will be dedicated people to collect and sort bugs, feature requests, etc. and prioritize
them with the long term product goal in mind. Each and every submission to alter the code will
be judiciously reviewed and only after the correctness and safety of the code is proved will it
be accepted.

------

#### How does FOSS projects make money?
- software development involves a lot of cost
- some of it is covered by donations
- some provide paid support
- some provide additional features for a fee

Note:
Starting with storing of the source code till making the final product available for download, a
software project incurs various costs. If everyone is working voluntarily, how is this cost met?
What is the motivation for people to work on it if there will be no salary? Well, many tools like
[GitHub](https://github.com) and GitLab allow free storage of source code for open source projects. The cost for them is
covered from the revenue earned from their paying customers. Many open source projects accept
donations and generate revenue through merchandise. Some open source projects tend to offer paid
support for people and industry. Some projects will also have a paid version in addition to the
open sourced one. The paid version will have more features and will also have an official support
channel where the needs of the paying customers will be addressed in a dedicated manner.

---

### Why is FOSS important?
- freedom of use/control
- increased security/privacy
- low/no cost
- customization
- reuse and efficiency
- but, I'm not a software professional...?

Note:
We are currently moving towards a subscription based culture. Whether it is software or something
as simple as watching a movie, everything is now available as subscriptions. This really blurs the
line between who owns the content. A few years back, if you pay some money, you would get a CD/DVD
of a movie which you can watch whenever you want for as long as the disk is usable. Now, if you want
to watch a movie, you have to keep paying the OTT platforms money every month. What you get is the
permission to watch it. You don't really own the movie.

But with FOSS, you get the freedom to own the software (without paying anything). You control how
the software works. You get to see how the software works internally and you can modify any part
that you don't like. With more eyes looking at the source code and validating every aspect of it,
the open source software tend to be more secure (or at least aware of the issues). Since the source
code is freely available, anyone can obtain it and build the software themselves, resulting in zero
cost of acquiring the software.

Another important advantage of FOSS projects is that it promotes reuse and reduces duplicate work.
If there's already an open source project that allows you to identify characters from an image, you
need not build the whole software from scratch to get an OCR software. If you're unhappy with the
algorithm used in the software, you can replace it with the algorithm of your choice and the new
OCR software is ready. Similarly, you will find open source projects that help you do a variety of
things without having to code anything yourself.

You might be thinking that you're not a professional software engineer, or you are not familiar with
the language in which it is written, why is having the source code freely available important to you.
You can still get the benefits of the open source software which is zero cost and high security. You
can also hire someone to verify the software for you. In case the maintainers decide to stop working
on the software for some reason, you can still obtain a copy of the source code and maintain it on
your own.

------

#### Drawbacks of FOSS
- security
- compatibility
- feature completeness
- continuation and availability

Note:
Though there are various advantages when using an open source software, it also comes with a bit of
disadvantages. The primary concern is the security of the software. We already mentioned in the last
section that since many people are verifying the code, it is easy to identify and fix issues. That is
a double edged sword. Not everyone who is looking at the source code might be having the good intention
of fixing the issue. Some might also be looking at the source code with the intention of identifying
any loopholes in the source code that they can exploit. Since the source code is open, it is also the
first components affected when a new security issue is identified.

Since the open source software are maintained in free time and/or without any financial motivation, the
support for platforms might be a bit limited. Some of the programs might not work outside a Linux based
environment. Some might not even work outside a specific Linux distribution. The features might not be
well rounded as compared to the proprietary couterpart due to lack of user feedback and/or lack of
time/skill for the contributors. It could also be possible that the developers of an open source project
abandon the project due to various reasons (lack of money, switching jobs, personal reasons, etc.). This
is a big risk. If the source code is not properly handed over to a successor, it could very well be possible
that even people who would want to keep the project alive by contributing to it might not be able to do so.
When there are several thousands of users for a project that gets abandoned, it will be a nightmare for
those people who depend on this open source project to either develop and equivalent solution or to find
another alternate open source/paid project that provides equivalent functionality.

---

### Why should you be part of FOSS?

------

#### Learning
- you can learn how bigger projects are
  - designed
  - developed
  - tested
  - released
  - documented
  - maintained
- you can learn how to read code

Note:
The first and foremost reason one should look at open source projects is for the learnings
that it can provide. Not matter how detailed your text books are, it cannot match real
experience and practice. By simply watching the development process followed in an open
source project, you can learn how a bigger software project is designed, developed, tested,
released, documented and maintained in the software industry. The open source projects are
usually at the cutting edge of the process and technology stack will be using the most prominent
technologies and principles followed across the software industry.

Another much important but underrated skill a software engineer must possess is the skill of
reading code. You might be thinking that it would be very easy to read another person's code
if you know all the syntax of the programming language. For example, C is a very simple language
with under 40 keywords and a bunch of operators. It also has only a few other concepts like
functions, arrays, structures and pointers. But is this sufficient to read and understand the
whole Linux kernel? When you have to read and understand a piece of code written by someone
else (whom you might not have even seen), you need to think at a much more abstract level rather
than looking at what's the meaning of each and every statement. This is a skill that can be
mastered with practice. Simply following an open source project closely will help you in
developing this skill.

------

#### Contributions
- open source contributions are valuable assets in interviews
- you get to feel how a typical IT company runs while you are in college
- whole community benefits from your contributions
- you can open source your projects and share the knowledge with the community

Note:
If you step up to the next level and decide to contribute to open source projects, that's a whole
new level. Having open source contributions listed in your CV/resume will have a huge positive
impact when you're attending placement drives - both in campus and outside. What this tells the
interviewer is that you are already familiar with (a) the tools, and (b) the processes that are
followed in the company and the effort and cost required to train you to be a productive employee
is much less compared to other people.

In addition to this immediate plus, you also get to know how a typical IT company works while you're
still in college. If you are able to identify any issues in an open source software or fix an already
identified issue, your few lines of code is going to make life easier for a lot of people who rely on
this open source project. If the issue that you identified/fixed is a security issue, you are making
the world a safer place.

---

### How you can be part of FOSS?

------

#### Using a version control software
- all the open source projects are maintained using version control software
- keeps track of the files in terms of the changes that are made to it
- common version control systems include Git, Subversion, Mercurial, etc.
- make a copy of the source code
- add the changes to your copy of source code
- submit the changes to the original source code repository

Note:
The general nature of operations is same across all open source projects. You will have a central
repository of source code. There will be a mechanism on top of that repository that is able to
track the changes that are made to the source code. There will be a system that can track the issues
that people report or are internally identified. This system will be able to track the changes that
are done with respect to each issue in the source code repository, along with details such as who
did the change and when. In general, you make a copy of this source code, add your changes on top
of it, test your changes (and add tests to your changes if required), and finally submit your changes
to the central repository. The source code management system will be able to smartly identify only the
changes that are made by you and request reviews/feedbacks from well established maintainers of the
project. The specific source code management tool used or what the process of submitting the changes
is called will differ based on projects, but the process remains the same.

------

#### What can you contribute?
- bug fixes
- features
- documentation
- process improvements

Note:
Depending on your comfort level with the code and the familiarity with the language and framework used
you can contribute to various topics. You can go through the list of issues that are already reported
and choose one that fits you. Usually, repositories mark issues based on the difficulty as "good first
issue" or "expert" or so on. You can also contribute a feature that is not already present in the
software. This would require a bit more expertise on the software and the programming language used to
build it. You can also contribute to an open source project by enhancing its documentation. Documentation
is also one of the important part of the product that a consumer relies on. You can contribute to the
documentation by submitting corrections, adding missing documentation for features, or even providing
translation of the documentation to a particular language. You can also contribute to the process
followed by an open source project. The process includes how users can report issues/request features,
what are the standards/best practices followed in the project, what is the process for submitting a
change request/modified code, what are the prerequisites required for a contributor, how the project is
compiled and bundled into a software product, etc.

---

### Demo

------

#### QEMU & UTM
- QEMU
  - virtualization software
  - can emulate i386, x86_64, arm, aarch64, ppc, ppc64, etc.
  - in-built disk image manager to handle virtual disk drives
  - command line utility
- UTM
  - a front-end for QEMU
  - abstracts all the command line options of QEMU under easy to understand GUI

------

#### Kubuntu
- Ubuntu with KDE Plasma desktop environment
- Beginner friendly and graphically similar to Windows
- Provides support for widgets
- Comes with Plasma based applications for common tasks

------

#### Zsh, Oh-My-Zsh, PowerLevel10k
- [`zsh`](https://sourceforge.net/p/zsh/code/ci/master/tree/) is an alternative to `bash`, the default shell in most GNU/Linux distributions
- [Oh-My-Zsh](https://github.com/ohmyzsh/ohmyzsh/) adds an easy to use plugin framework and a bunch of useful plugins on top of `zsh`
- [PowerLevel10k](https://github.com/romkatv/powerlevel10k) is a theme for Oh-My-Zsh which gives a "cool looking" yet functional and feature rich terminal experience

Note:
1. QEMU, UTM
2. Kubuntu: KDE plasma, widgets, settings, Dolphin, Kate
3. Zsh, OhMyZsh, Powerlevel10k
4. libreoffice
5. TeX with Kile
6. Blender
7. Audacity
8. JGraph
9.  Numpy, Scipy, Pandas, Plotly
10. Octave
11. OBS Studio
12. VS Code

---

### References

------

#### For this presentation
- Slides prepared using [reveal.js](https://github.com/hakimel/reveal.js)
- Edited in [Visual Studio Code](https://github.com/microsoft/vscode)
- Index page prepared using [Bootstrap](https://github.com/twbs/bootstrap)
- Slides are hosted using [GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/about-github-pages)
- Source code for this slide available in [GitHub](https://github.com/anthoor/slides/tree/main/foss)

------

#### Further reading
- [Free Software Foundation](https://www.fsf.org/)
- [Free and Open Source Software](https://en.wikipedia.org/wiki/Free_and_open-source_software)
- [GNU/Linux Distribution Timeline](https://futurist.se/gldt/wp-content/uploads/12.10/gldt1210.svg)
- [What is FOSS? - An article from It's FOSS](https://itsfoss.com/what-is-foss/)

------

#### Version control software
- [Git](https://git-scm.com/)
- [Subversion](https://subversion.apache.org/)
- [Mercurial](https://www.mercurial-scm.org/)
- [Bazaar](https://bazaar.canonical.com/en/)

------

#### Source code for popular languages and frameworks - I
- [Java](https://github.com/openjdk/jdk)
  - [Tomcat](https://github.com/apache/tomcat)
  - [Spring Boot](https://github.com/spring-projects/spring-boot)
  - [Hibernate](https://github.com/hibernate/hibernate-orm)
  - [Quartz](https://github.com/quartz-scheduler/quartz)
- [Python](https://github.com/python/cpython)
  - [Django](https://github.com/django/django)
  - [TensorFlow](https://github.com/tensorflow/tensorflow)
  - [Numpy](https://github.com/numpy/numpy)
  - [Pandas](https://github.com/pandas-dev/pandas)
  - [Plotly](https://github.com/plotly/plotly.py)

------

#### Source code for popular languages and frameworks - II
- [Golang](https://github.com/golang/go)
  - [Gin](https://github.com/gin-gonic/gin)
  - [Cobra](https://github.com/spf13/cobra)
  - [podman](https://github.com/containers/podman)
  - [kubernetes](https://github.com/kubernetes/kubernetes)
  - [hugo](https://github.com/gohugoio/hugo)
- [Kotlin](https://github.com/JetBrains/kotlin)
- [Rust](https://github.com/rust-lang/rust)

------

#### Source code for popular programs
- [Firefox](https://hg.mozilla.org/mozilla-central/file)
- [Octave](https://hg.savannah.gnu.org/hgweb/octave)
- [libreoffice](https://gerrit.libreoffice.org/q/project:core)
- [Blender](https://git.blender.org/gitweb/gitweb.cgi/blender.git)
- [Audacity](https://github.com/audacity/audacity)
- [TeX Live](https://tug.org/svn/texlive/trunk/)

------

#### Source code for operating systems
- [Linux kernel](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/tree/)
- [Debian](https://sources.debian.org/)
- [ubuntu](https://code.launchpad.net/ubuntu)
- [GNOME](https://gitlab.gnome.org/GNOME?sort=stars_desc)
- [KDE Plasma](https://invent.kde.org/plasma)
- [Android](https://cs.android.com/android/platform/superproject/)
