# How to use Google Optimize [Work in Progress]
<img width="1900" alt="google-analytics-logo" src="https://github-cloud.s3.amazonaws.com/assets/4185328/10566203/1ccc209e-75d8-11e5-964c-57449ca02506.png">

## Outline
  + [What?](#what)
  + [Why?](#why)
  + [Before you Start](#before-you-start)

## What?
[Google Optimize (GO)](LINKYLINKHERE) is a free tool provided by Google as part
of [Google Analytics](analytics.google.com).

It **allows you to set up [A/B, multivariate or redirect tests](https://github.com/iteles/learn-ab-and-multivariate-testing)** to
determine whether changes made to your web pages/apps are moving you towards your
[pre-determined goals](https://github.com/iteles/learn-ab-and-multivariate-testing#2-what-is-your-goal) or away from them.

This 'how to' **assumes you already know the basics of A/B or multivariate
testing** along with the required terminology, but if not, you can _read our
introduction_ here: https://github.com/iteles/learn-ab-and-multivariate-testing.

## Why?
If you found this page, you probably already agree that A/B testing is something
you want to try.
The _'Why?'_ we're answering here is 'Why use Google Optimize?':

+ It's **free** which makes it a **good starting point** for the bootstrapped
startup or the individual looking to get some testing practice
+ It's **reliable** provided you **know how to use it** and analyse the results
correctly
+ Setup is relatively easy and quick for full page 'redirect' tests, as well as
for more specific, smaller A/B tests

## Before you Start

### Understand what you want to achieve
Our your problem areas, set your goals, formulated your hypothesis and designed
your variations.
If you need some help with this, we've written a
[Getting Started with A/B testing](https://github.com/iteles/learn-ab-and-multivariate-testing#getting-started) step-by-step for you.

### What you need to know about Google Optimize
Google Optimize allows you to run three different types of tests:
+ **Redirect** tests allow you to **test full pages** against each other. This
means that if you want to test a change in button text, you'll need to produce a
duplicate of the **whole page you're testing** and change the text on just that
button. Redirect tests really come into their own when used to test large site
redesigns. One pitfall of redirects is that you'll have a **different ending to
your [URL](http://dictionary.reference.com/browse/url)** for each page you test
(e.g. `www.example.com` for one variation and `www.example.com/welcome` for
another)
+ **A/B** tests give you more specific control over the elements and text that
you want to test, perfect for tests like the button example above. Optimize comes
with a really handy Chrome extension that allows you to make changes to the
HTML/CSS/text of any test page and then create tests based on those changes.
+ **Multivariate:** WiP


## Setting up your experiment
[Work in Progress]

To set up an experiment first you'll need a

### While the experiment is happening
You should _continually assess your priorities_. These are **suggested steps**
but not hard and fast rules for _every_ situation.
+ Plan what your next experiment will be if your challenger fails or if it 'wins'
(compared to the _control_)
  + Start by aiming to improve on your winner rather than moving immediately onto a completely different experiment

### After the experiment
+ **Remember:** Just because a specific design 'won' in an experiment doesn't
make it untouchable - don't be afraid of making it the control in further
experiments with new ideas
+ Try to have someone **responsible for shipping the changes** - if you just
'provide recommendations for change' based on your experiment results, they may
just get lost

## To-Do
+ [ ] Is multi-armed bandit it still opt out?
+ [ ] Discuss keeping close eye on experiments


+ [ ] Make a note of the kill switch (to cut losses when experiment goes poorly)
+ [ ] Research Optimize/Content Experiments' [API](https://developers.google.com/analytics/solutions/experiments-feature-reference)

## Resources
+ http://rich-page.com/website-optimization/google-content-experiments-12-must-knows-before-using/
+ https://brianclifton.com/blog/2013/09/24/google-content-experiments/
+ https://www.quora.com/What-are-the-practical-drawbacks-of-multi-armed-bandit-testing-as-applied-to-conversion-optimization

**Tips to improve your testing:**
+ http://marketingland.com/12-tips-to-take-your-ab-multivariate-testing-to-the-next-level-50249
+ also for interpreting your results section: http://www.optimizeandprophesize.com/jonathan_mendezs_blog/2008/05/multivariate-te.html
+ and https://econsultancy.com/blog/6740-what-your-mother-never-taught-you-about-multivariate-testing/

### Possible FAQ
+ Should I choose A/B or MVT?
