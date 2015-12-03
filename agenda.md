# Itinerary

## Monday 2015-12-07
 * 10:00 - 10:10 :: welcome
 * 10:10 - 12:00 :: discussion of mechanics of collaboration (inc coffee break + cookies)
 * 12:00 - 13:00 :: lunch
 * 13:00 - 14:00 :: discussion, continued
 * 14:00 - 16:00 :: training on collaboration tools used by the scipy ecosytem (inc coffee break + cookies)
 * 16:00 - 16:30 :: Kerstin Kleese Van Dam on streaming
 * 16:30 - 17:00 :: Ray Osborn on file formats

## Tuesday 2015-12-08
 * 09:00 - 10:30 :: short presentations from all facilities
 * 10:30 - 12:00 :: self-organize into work groups and begin work
 * 12:00 - 13:00 :: working lunch with stand-up reports from all work-groups
 * 13:00 - 16:30 :: work time (coffee + cookies)
 * 16:30 - 17:00 :: report with slides from each work-group

## Wednesday 2015-12-09
 * 09:00 - 12:00 :: work time (coffee + cookies)
 * 12:00 - 13:00 :: working lunch with stand-up reports from all work-groups
 * 13:00 - 16:30 :: work time (coffee + cookies)
 * 16:30 - 17:00 :: report with slides from each work-group

## Thursday 2015-12-10
 * 09:00 - 12:00 :: work time (coffee + cookies)
 * 12:00 - 13:00 :: working lunch with stand-up reports from all work-groups
 * 13:00 - 16:30 :: work time (coffee + cookies)
 * 16:30 - 17:00 :: report with slides from each work-group

## Friday 2015-12-11
 * 09:00 - 10:30 :: final work (coffee + cookies)
 * 10:30 - 12:00 :: final presentations, lessons learned, etc

# Detailed Outline for Monday

## Welcome
* Quick introductions: everyone say your name and affiliation
* We will begin by building a consensus on the mechanics of an inter-facility
software collaboration of scientific Python libraries for data analysis at
lightsources. The astronomy community provides us with a successful model, astropy.

## Vision
Take a few minutes right now to read astropy vision document:
http://docs.astropy.org/en/stable/development/vision.html

Should we adopt a variation on this document as our vision for inter-facility
collaboration?

We prepared a lightly edited version (essentially, 'astro' -> 'xray'). Comments?

## Standards
Basic standards for “affiliated projects” can be minimal:
http://www.astropy.org/affiliated/#affiliated-instructions

The core package is held to a higher standard, like other core scipy packages.
Examples from related projects:

* http://docs.astropy.org/en/stable/development/codeguide.html
* http://scikit-image.org/docs/stable/contribute.html
* http://matplotlib.org/devel/coding_guide.html

From our perspective, the key points are:
* Make simple, composable functions to enable code re-use.
* Keep I/O logic, visualization logic, and scientific logic separate.
* Isolate dependencies. (Top-level package should require only numpy, scipy, matplotlib, pandas.)
* Use basic types: built-in Python types + numpy arrays -- e.g., no special “Image”
object for example

## Naming the project
Does anyone have a better idea than “scikit-xray”? Context: What is a scikit?
http://scikits.appspot.com/scikits

(The package name “xray” is already taken, and it has nothing to do with
X-rays.)

## Reasons for using and GitHub
* Everyone is moving to git and GitHub to enable distributed collaboration,
including the Python scientific stack. We’ll contributing to upstream projects
like scikit-image, so we’ll be using it anyway.
* Pre-merge review and diff comments are hugely important for successful collaboration.
* It integrates nicely with DOI generation, automated tests, auto-built documentation, etc.

## Detailed Mechanics of Collaboration

### Packaging (Distribution)
We like conda, but we should support any package distribution systems that
people need.
History of conda, what is does

What other packaging systems would we need to support?

### Documentation

#### Standards
To borrow from
http://swcarpentry.github.io/good-enough-practices-in-scientific-computing/
every file and function should have a brief explanatory remark at the start and
at least one working example of its use.

#### Mechanics
At NSLS-II, we use sphinx, which inspects Python source code to auto-generate
API documentation (in addition to prose documentation). It is the common choice
for other scientific Python packages.

We also like example Jupyter notebooks. Many very new tools (see
[tmpnb](https://try.jupyter.org/), [binder](mybinder.org),
[thebe](https://oreillymedia.github.io/thebe/)) allow users to experiment
with scientific Python analysis code in the browser with no installation at
all.

### Testing
Testing is essential for effective collaboration.

#### Testing Philosophy
* If you don’t want a contributor to break your code, protect it with a test.
* If you find a bug, make a test to prove that you fixed it.

#### Testing Machinery
* How TravisCI/appveyor/CircleCI works
* We can test on both synthetic data (preferred, but usually more work) and real
data.
* Following astropy, bundle small data files with the code ( < 100 kb) and
provide convenient functions for downloading any large data files.
* There is interesting to be done in finding good ways to test scientific code:
sensitivity testing, generative testing, ….

## Git Tutorial
* Deputize everyone who already knows git.
* Follow SWC tutorial: http://swcarpentry.github.io/git-novice/

