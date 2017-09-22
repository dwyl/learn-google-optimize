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


+ The first thing to do to set up Google Optimize is going to be to add these code snippets right at the top of the `head` of the page you want to test. Don't worry, we'll fill the codes in later.

```html
<!-- this code snippet will stop your original version flashing up before your variant -->
<style>.async-hide { opacity: 0 !important} </style>
<script>(function(a,s,y,n,c,h,i,d,e){s.className+=' '+y;h.start=1*new Date;
h.end=i=function(){s.className=s.className.replace(RegExp(' ?'+y),'')};
(a[n]=a[n]||[]).hide=h;setTimeout(function(){i();h.end=null},c);h.timeout=c;
})(window,document.documentElement,'async-hide','dataLayer',4000,
{'GTM-PFH9FWG':true});</script>
<!-- end snippet -->
<!-- Google Analytics -->
<script>
(function(i,s,o,g,r,a,m){i['GoogleAnalyticsObject']=r;i[r]=i[r]||function(){
(i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new Date();a=s.createElement(o),
m=s.getElementsByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m)
})(window,document,'script','https://www.google-analytics.com/analytics.js','ga');

ga('create', '<FILL THIS IN LATER>', 'auto');
ga('require', '<FILL THIS IN LATER>');
ga('send', 'pageview');
</script>
<!-- End Google Analytics -->
```

+ You're going to need to create an account on [Google Optimize](timize.google.com) and [Google Analytics](https://analytics.google.com/analytics/web/)
+ On the Optimize dashboard click on "Create Experiment"
+ Add the name of the experiment and the url of the page you wish to do the experiment on
+ Now you're going to need to create a property on Google Analytics, google has a really good guide for this so I'll leave it to them to show you how! : https://support.google.com/analytics/answer/1042508?hl=en
+ Put the tracking id from your property in the google analytics snippet in your code, right here:
```js
ga('create', '<FILL THIS IN LATER>', 'auto');
```
+ Select the property you just made in the Optimize dashboard
+ You'll be prompted with "get optimize snippet", this is the code we have pasted at the top of our html already. Still click through as it will give you a code you need.
+ Take the code given to you (starting with "GTM") and pop it into your snippet, here:
```js
ga('require', '<FILL THIS IN LATER>');
```
+ Click on your experiment to open it up
+ In the bottom left link your property
+ Add in an objective (We'll be going for session duration)
+ Add a hypothesis of what you expect, this is an experiment afterall!
+ Click on add a variant
+ Then click the arrow to edit your variant.
+ At this point you should be prompted to install the Chrome Optimize plugin, just click through and install it.
+ The editor has a really nice interface. you can click on an element and change the html, so you can add some classes. This works super well with tachyons! you can also add extra CSS classes by clicking `<>`.
+ You can make a small change, or even add loads more HTML into the body if you want a big change
+ Click save and then click done when you've made your changes
+ You can always add more variants or edit the ones that are there before you start the experiment, but once it's started you can't update anything, you're locked in to your choices, and you can't pause the experiment, only stop it and start a whole new one, so make sure you're happy with your variants!
+ If you've done this all correctly then you'll have an option to start your experiment. If you're all ready, go ahead and click start!
+ Your experiment is started!
+ now, open your site in your browser, and open an incognito window with the same site, and hopefully you'll have both variants! It's a 50/50 chance so if you don't get the variant in either window just close the incognito window and open it again, and go back to your site. (you have to close and open the incognito window, not just refresh so that it acknowledges them as 2 separate sessions. Optimize is smart and wont send the same session to two different versions of the same page, that's confusing" )
+ Same url, 2 different versions!


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



+ first take your site and add the code snippets at the top of the head (we'll be filling in the unique ids later)
+ create an account on google optimize and google analytics
+ click "create experiment"
+ add the name of the experiment and the url of the page you will be playing with
+ now you're going to need to create a property
+ https://support.google.com/analytics/answer/1042508?hl=en
+ put the tracking id from your property in you google analytics snippet (as the second argument to the ga function whos first argument is `create`)
+ select your property in google optimize and link it
+ you'll be prompted with "get optimize snippet". do it. and follow the instructions on screen
+ You will now have a code starting with `UA` being passed to the create function and a code starting with `GTM` being passed to the require function
+ You now need to install the optimize chrome plugin, you will be prompted to do so, install it
+ open your experiment
+ link your property
+ add an objective (we'll be doing session duration)
+ add a hypothesis
+ add a variant
+ edit your variant
+ The editor has a really nice interface. you can click on an element and change the html, so you can add some classes. This works super well with tachyons! you can also add extra CSS classes by clicking `<>`.
+ You can make a small change, or even add loads more HTML into the body if you want a big change
+ click save and then done when you've made you changes
+ If you've done this all correctly then you'll have an option to start your experiment. If you're all ready, go ahead and click start!
+ You can always add more variants or edit the ones that are there before you start the experiment, but once it's started you can't update anything, you're locked in to your choices, and you can't pause the experiment, only stop it and start a whole new one, so make sure you're happy with your variants!
+ your experiment is started!
+ now, open your site in your browser, and open an incognito window with the same site, and hopefully you'll have both variants! It's a 50/50 chance so if you don't get the variant in either window just close the incognito window and open it again, and go back to your site. (you have to close and open the incognito window, not just refresh so that it acknowledges them as 2 separate sessions. Optimize is smart and wont send the same session to two different versions of the same page, that's confusing")
+ same url, 2 different versions!
