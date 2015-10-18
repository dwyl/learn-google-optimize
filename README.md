# How to use Google Content Experiments
<img width="1900" alt="google-analytics-logo" src="https://github-cloud.s3.amazonaws.com/assets/4185328/10566203/1ccc209e-75d8-11e5-964c-57449ca02506.png">

## Outline
  + [What?](#what)
  + [Why?](#why)
  + [Before you Start](#before-you-start)

## What?
[Google Content Experiments](https://support.google.com/analytics/answer/1745147) is a free tool provided by Google as part of [Google Analytics](analytics.google.com). 
 
It **allows you to set up [A/B or multivariate tests](https://github.com/iteles/learn-ab-and-multivariate-testing)** to determine whether changes made to your web pages/apps are moving you towards your [pre-determined goals](https://github.com/iteles/learn-ab-and-multivariate-testing#2-what-is-your-goal) or away from them.

This 'how to' **assumes you already know the basics of A/B or multivariate testing** along with the required terminology, but if not, you can _read our introduction_ here: https://github.com/iteles/learn-ab-and-multivariate-testing.

## Why?
If you found this page, you probably already agree that A/B testing is something you want to try.
The _'Why?'_ we're answering here is 'Why use Content Experiments (CE)?':

+ It's **free** which makes it a **good starting point** for the bootstrapped startup or the individual looking to get some testing practice
+ It's **reliable** provided you **know how to use it** and analyse the results correctly
+ Setup is relatively easy and quick for full page A/B tests

## Before you Start

### Understand what you want to achieve
Our your problem areas, set your goals, formulated your hypothesis and designed your variations.
If you need some help with this, we've written a [Getting Started with A/B testing](https://github.com/iteles/learn-ab-and-multivariate-testing#getting-started) step-by-step for you.

### What you need to know about Content Experiments
+ Unlike some more _detailed_ and much more _expensive_ tools, CE only allows you to **test full pages** against each other
  + This means that if you want to test a change in button text, you'll need to produce a duplicate of the **whole page you're testing** and change the text on just that button (rather than telling CE to change that one small thing for you)
  + _**Consequences:**_
    + You'll have a **different ending to your [URL](http://dictionary.reference.com/browse/url)** for each page you test (e.g. `www.example.com` for one variation and `www.example.com/welcome` for another)
    + You'll need to **manually keep track** of the changes you made to your [control](https://github.com/iteles/learn-ab-and-multivariate-testing#terminology) 
+ Watch out for the **multi-armed bandit**!






## To-Do
+ [ ] Research multi-armed bandit and most recent defaults - is it still opt out?
+ [ ] Discuss keeping close eye on experiments


+ [ ] Make a note of the kill switch (to cut losses when experiment goes poorly)
+ [ ] Research CE's [API](https://developers.google.com/analytics/solutions/experiments-feature-reference)

## Resources
+ http://rich-page.com/website-optimization/google-content-experiments-12-must-knows-before-using/
+ https://brianclifton.com/blog/2013/09/24/google-content-experiments/

