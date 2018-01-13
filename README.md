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

To do an experiment you will need the Chrome browser, and a live website, which you have control over the code of.

## Setting up an A/B test

The first thing to do to set up Google Optimize is going to be to add these code snippets right at the top of the `head` of the page you want to test. Don't worry, we'll fill the codes in later.

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

You're going to need to create an account on [Google Optimize](timize.google.com) and [Google Analytics](https://analytics.google.com/analytics/web/)
On the Optimize dashboard click on "Create Experiment"

![my container experiments - optimize - google chrome_024](https://user-images.githubusercontent.com/21139983/30806666-9fa25968-a1ee-11e7-9fe2-7a4749a5c45a.png)

Add the name of the experiment and the url of the page you wish to do the experiment on

![my container experiments - optimize - google chrome_025](https://user-images.githubusercontent.com/21139983/30806669-9fb38ad0-a1ee-11e7-84a8-814defb3c26d.png)

Now you're going to need to create a property on Google Analytics, google has a really good guide for this so I'll leave it to them to show you how! : https://support.google.com/analytics/answer/1042508?hl=en

Put the tracking id from your property in the google analytics snippet in your code, right here:

```js
ga('create', '<FILL THIS IN LATER>', 'auto');
```

Select the property you just made in the Optimize dashboard

![my container experiments - optimize - google chrome_027](https://user-images.githubusercontent.com/21139983/30806667-9faf8a52-a1ee-11e7-9412-a959c04dd70b.png)

You'll be prompted with "get optimize snippet", this is the code we have pasted at the top of our html already. Still click through as it will give you a code you need.

Take the code given to you (starting with "GTM") and pop it into your snippet, here:

```js
ga('require', '<FILL THIS IN LATER>');
```

Click on your experiment to open it up
In the bottom left link your property

![my-awesome-experiment details - optimize - google chrome_031](https://user-images.githubusercontent.com/21139983/30806660-9f8ebf48-a1ee-11e7-9650-75880423d286.png)

![my-awesome-experiment details - optimize - google chrome_033](https://user-images.githubusercontent.com/21139983/30806665-9f9f8882-a1ee-11e7-9e54-5ec803e689bd.png)

Add in an objective (we'll be going for session duration)

![my-awesome-experiment details - optimize - google chrome_034](https://user-images.githubusercontent.com/21139983/30806662-9f9b7dbe-a1ee-11e7-94df-50ebc81c070e.png)

Add a hypothesis of what you expect, this is an experiment afterall!
Click on "New Variant"

Give your variant a relevant and memorable name!

Then click on "0 changes" to edit your variant.

![my-awesome-experiment details - optimize - google chrome_036](https://user-images.githubusercontent.com/21139983/30806664-9f9c07d4-a1ee-11e7-8e61-dd8b24397689.png)

At this point you should be prompted to install the Chrome Optimize plugin,
just click through and install it.

The editor has a really nice interface. you can click on an element, then click
"Edit Element" to change the HTML, so you can add some classes. This works
super well with [tachyons](https://github.com/dwyl/learn-tachyons)! you can
also add extra CSS classes by clicking `<>`.

![document - google chrome_037](https://user-images.githubusercontent.com/21139983/30806659-9f7c324c-a1ee-11e7-9870-990c48eff821.png)

You can make a small change, or even add loads more HTML into the body if you
want a big change

Click save and then click done when you've made your changes
You can always add more variants or edit the ones that are there before you
start the experiment, but once it's started you can't update anything, you're
locked in to your choices, and you can't pause the experiment, only stop it and
start a whole new one, so make sure you're happy with your variants!

If you've done this all correctly then you'll have an option to start your
experiment. If you're all ready, go ahead and click start!

![my-awesome-experiment details - optimize - google chrome_040](https://user-images.githubusercontent.com/21139983/30806663-9f9bd8b8-a1ee-11e7-9843-f82a1f98ead4.png)


Your experiment is started!

now, open your site in your browser, and open an incognito window with the same
site, and hopefully you'll have both variants! It's a 50/50 chance so if you
don't get the variant in either window just close the incognito window and open
it again, and go back to your site. You have to close and open the incognito
window, not just refresh so that Chrome acknowledges them as 2 separate
sessions. Optimize is smart and wont send the same session to two different
versions of the same page, that's confusing.

As you can see below, we have the same url, with 2 different versions!

![workspace 1_024](https://user-images.githubusercontent.com/21139983/30806668-9fafb1d0-a1ee-11e7-8630-64749885781e.png)

## Setting up a Multivariate test
Start a new experiment, this time selecting "Multivariate" rather than A/B
test.

![my container experiments - optimize - google chrome_025](https://user-images.githubusercontent.com/21139983/30857717-bf56d740-a2b4-11e7-9aa1-f491e73509e3.png)

Click on your new experiment to enter the dashboard.

Add and objective and hypothesis, just as you would for the A/B test
Now you're going to be adding your variants, this is where things are different!

![multivariate-practice details - optimize - google chrome_026](https://user-images.githubusercontent.com/21139983/30857720-bf5b8c40-a2b4-11e7-8ab2-47a6dd01d4af.png)

Each section is one set of variables, so the variants within each section will never be combined with eachother, but they will be combined with all of the variants of all of the other sections.

Editing a variant is exactly the same as it is for an A/B test.

We're going to add 2 extra options for the colour of the button and 2 extra
options for the call to action, which totals 3 for each including the original
controls, and Optimize tells us how many total options we have, in this case, 9.

![multivariate-practice details - optimize - google chrome_028](https://user-images.githubusercontent.com/21139983/30857719-bf59dde6-a2b4-11e7-8d68-c761fedcb304.png)

If you want to see what the different combinations look like you can click on
the Combinations tab. You can click on the image of a screen with a phone, and it will give you the option to preview the combination, if you click "Web Preview" you will have your page loaded with that combination on it.

This preview will stay active on your page until deactivated, so anyone visitng will see this variant. To deactivate it, click the (now blue) screen icon again and select "Turn Off Preview".

It can be worth checking all of them just to make sure they are as you expect them to be, as you won't be able to change them once the experiment has started.   

![multivariate-practice details - optimize - google chrome_029](https://user-images.githubusercontent.com/21139983/30857718-bf577628-a2b4-11e7-88ce-721e3c8cf977.png)

Once you've set all of this up, you can start your experiment!

It would take a while and be annoying to have load up every variant by
opening and closing incognito windows, but as long as you get one variant other
than your original in a different session then you know that your experiment is working :+1:.

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


## Resources
+ If you prefer to learn from videos then here is a really good video tutorial
on setting up an A/B test with Google Optimize:
https://www.youtube.com/watch?v=vDDMMbhvSVU

**Tips to improve your testing:**
+ http://marketingland.com/12-tips-to-take-your-ab-multivariate-testing-to-the-next-level-50249
+ also for interpreting your results section: http://www.optimizeandprophesize.com/jonathan_mendezs_blog/2008/05/multivariate-te.html
+ and https://econsultancy.com/blog/6740-what-your-mother-never-taught-you-about-multivariate-testing/

### FAQ
#### Should I choose A/B or MVT?
For more information on the differences between, and different use cases of A/B and Multivariate testing then we recommend having a look at our [`learn-ab-and-multivariate-testing`](https://github.com/foundersandcoders/international/issues/156) repo.
