---
layout: post
title: New site using Jekyll and Github Pages
comments: trues
excerpt: I've never considered myself a front-end developer. But maybe today that changes, a little bit. I wanted to share some of the tools I used to get this site up and running in about a week.
---

#New site using Jekyll and Github Pages

I've never considered myself a front-end developer. But maybe today that changes, a little bit. With great direction from friend and colleague [Erik Mitchell](http://www.twitter.com/mitc0185), I starting playing around with Jekyll. It took a while to get it working, but once it was, I barely had to think about it again.

##I wanted to share some of the tools I used to get this site up and running in about a week.

###Jekyll
Jekyll builds and locally serves my site. This was basically all new to me. **To install Jekyll**, I followed directions at their [main site](http://www.jekyllrb.com).

Additionally, I found Andy Taylor's [post on the topic](http://andytaylor.me/2012/11/03/installing-ruby-and-jekyll/) helpful.

Since **using the terminal** was relatively new to me as well, this [for Dummies page](http://www.dummies.com/how-to/content/how-to-use-basic-unix-commands-to-work-in-terminal.html) was helpful throughout. The one thing those posts may not mention is the need for the `sudo` command before most terminal commands like `gem install jekyll`. The `sudo` command means you're overriding any commands that wouldn't typically have admin access, and because of this, you will need to enter an admin password. There's probably a way to unlock things so `sudo` isn't always needed, but I never got that far.

The Jekyll site contains much of the rest of the information you need to get up and running, but when it comes to **writing posts in markdown**, you'll want to check out the [official site](http://daringfireball.net/projects/markdown/) for Markdown language. I'm still getting used to it, so sometimes I pepper in HTML when I can't figure something out, or when Markdown doesn't support what I need to show. It's great that this system allows you to use both Markdown and HTML in the same .md document.


###Twitter Bootstrap
Confession: I totally love [Twitter Bootstrap](http://www.getbootstrap.com). The developers I work with at HealthPartners have adapted it for our authenticated site, meaning I can rapid prototype at work. Anytime I need to stand up a site quickly, I immediately go to Bootstrap. You don't have to touch the CSS to quickly create something that looks nice on any device, but it's also built so that playing with styles or applying a theme is easy.

**Getting up and running with bootstrap** is as simple as plopping the CSS and JS folders into your site structure, and linking to it in the header and footer, respectively. Viewing the source of one of [their examples](http://getbootstrap.com/getting-started/#examples) is honestly one of the best ways to understand how you can start structuring the HTML to fit your needs.

I also **borrowed a great little chunk of CSS** from dev friends at HealthPartners that lets you quickly adjust padding on any element by adding a couple of classes. With this CSS, all you need to do is indicate the direction of the padding (ex. `pad-top`, `pad-right`) and the size (ex. `jumbo`, `mini`, `sm`) if you're not happy with the default of 15px.


<div class="panel-group" id="accordion">
  <div class="panel panel-default">
    <div class="panel-heading">
      <h4 class="panel-title">
        <a data-toggle="collapse" data-parent="#accordion" href="#collapseOne">
          CSS padding classes<span class="pull-right"><em>click to expand</em></span>
        </a>
      </h4>
    </div>
    <div id="collapseOne" class="panel-collapse collapse">
      <div class="panel-body">
      	<pre>
			<code>
/* Padding modifications for Bootstrap, adapted from HealthPartners */

.pad-top {
	padding-top: 15px;
}
.pad-top.mini {
	padding-top: 4px;
}
.pad-top.sm {
	padding-top: 8px;
}
.pad-top.medium {
	padding-top: 11px;
}
.pad-top.large {
	padding-top: 23px;
}
.pad-top.extra-large {
	padding-top: 35px;
}
.pad-top.jumbo {
	padding-top: 45px;
}
.pad-top.extra-jumbo {
	padding-top: 55px;
}
.pad-bottom {
	padding-bottom: 15px;
}
.pad-bottom.mini {
	padding-bottom: 4px;
}
.pad-bottom.sm {
	padding-bottom: 8px;
}
.pad-bottom.medium {
	padding-bottom: 11px;
}
.pad-bottom.large {
	padding-bottom: 23px;
}
.pad-bottom.extra-large {
	padding-bottom: 35px;
}
.pad-bottom.jumbo {
	padding-bottom: 45px;
}
.pad-bottom.extra-jumbo {
	padding-bottom: 55px;
}
.pad-left {
	padding-left: 15px;
}
.pad-left.mini {
	padding-left: 4px;
}
.pad-left.sm {
	padding-left: 8px;
}
.pad-left.medium {
	padding-left: 11px;
}
.pad-left.large {
	padding-left: 23px;
}
.pad-left.extra-large {
	padding-left: 35px;
}
.pad-left.jumbo {
	padding-left: 45px;
}
.pad-left.extra-jumbo {
	padding-left: 55px;
}
.pad-right {
	padding-right: 15px;
}
.pad-right.mini {
	padding-right: 4px;
}
.pad-right.sm {
	padding-right: 8px;
}
.pad-right.medium {
	padding-right: 11px;
}
.pad-right.large {
	padding-right: 23px;
}
.pad-right.extra-large {
	padding-right: 35px;
}
.pad-right.jumbo {
	padding-right: 45px;
}
.pad-right.extra-jumbo {
	padding-right: 55px;
}
	</code>
</pre>
</div>
</div>
</div>
</div>
<br />
Because I've used Bootstrap a lot, I wanted to start with a look that was still simple, but looked a little different than the default. I **added a free Bootstrap theme** from [Bootswatch](http://bootswatch.com/) called "Yeti". I plan to eventually mold this site into something more distinct, but in order to get this thing out quickly while I was on vacation, using a theme made the most sense. There are also plenty of themes out there you can buy if you really don't want to touch the visual design.

###Github and Github Pages
Github is a great way to **add version control** to any of your projects. I also love that it displays your activity on your [personal page](http://www.github.com/linoleumtile)... kind of a nice way to see when you've been active and maybe even [hold yourself accountable](https://twitter.com/jeresig/status/412402730091569152). I know a lot of people who use github via terminal commands, but again, that's still pretty new to me. Luckily there is a [github client for mac](http://mac.github.com/), and it is awesome! I have the best luck when I **start a new repository in github** before producing any files for a project. 

The other great thing about using Github and Jekyll together is that you can **host simple sites using [Github pages](http://pages.github.com/)**. By following the simple directions, everytime I synced my commits on github, they would appear on [linoleumtile.github.io](linoleumtile.github.io). Rumor has it that you can even point your own URL to this, so that will be my next adventure!

###Other great tools
I've always thought [Disqus](http://www.disqus.com/) seemed like a great platform, so I decided I would try it out. To my great surprise, it was the simplest thing I've done to build up this website, **taking less than 5 minutes to install commenting functionality**. SO EASY. 

Finally, I'm **testing out a simple sharing service** called [ShareThis](http://www.sharethis.com). I don't know much about it, and am open to suggestions for other things that are out there, or glowing recommendations if it really is "Best in Class".

<hr/>

Did I miss something? Let me know in the comments below. 

<br />[&lt; Back home](/)<br /><br />
