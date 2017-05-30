---
layout: post
title:  "nil is not nothing"
date:   2013-08-05 07:56:00
categories: nil ruby coding
---
<div class="postmetadata">
  Posted on <span class="updated">August 05, 2013</span>
</div>

Programming will always be a representation of reality. It can never be the real thing. For example, you may have a relationship with your bank, where your money flows in and out, but the program you access online to interact with your bank merely represents your banking data and the methods you call to manipulate that data.

In essence, every program tries to 'represent' the real world and our interaction with that world. One can also see this behavior in programming languages themselves.

In Ruby, `nil` is that quintessential thing known as nothingness. If something is nil in your program, the computer sees it as 'not existing'. But this isn't quite true--at least in Ruby.

Nil *is* something. In fact, it's a reference to nothing, a representation of reality. We can't contain something as nothing without defining it and making it tangible. In Ruby (like everything else) nil is an object.

{% highlight fancy %}
nil.object_id
=> 4
something = nil
something.object_id
=> 4
{% endhighlight %}

We can take this even further when we put nothing into an array. If nil were truly 'nothing', wouldn't the array be empty?

{% highlight fancy %}
an_array = []
an_array.empty?
=> true
an_array = [nil]
an_array.empty?
=> false
{% endhighlight %}

It's hard to represent nil without making it exist--how else would we utilize it in our programs? When something is truly non-existent in our code, we get errors.

{% highlight python %}
>> something
=> nil
>> undefined_variable
NameError: undefined local variable or method
 'undefined_variable' for main:Object
{% endhighlight %}

And so, like many things in our ever-increasing [copy world][copy-world], nil is just a copy of something that means nothing. And by creating that copy, we've created something that most certainly exists.

[copy-world]: https://medium.com/we-live-in-the-future/53db59f5571
