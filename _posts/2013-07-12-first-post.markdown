---
layout: post
title:  "Start a New Blog"
date:   2013-07-12 09:05:00
categories: new blog
---
What better way to start off a new blog than by making the first post about writing a blog? Okay, that's a bit too meta, so I'll explain why I'm writing this blog in the first place.

Never stop writing! A screenwriter teacher once told me that, and I believe it to be true. Although I don't write much screenplays anymore, I do practice writing scripts :)

I won't go into the full details of how I got here. Basically, I started out in the technology industry and soon left to try producing movies in Hollywood. Like many, I found the star-gleaming grind to be unfulfilling and miserable, so I came back to San Francisco and started learning code.

I got excited about the infinite possiblities of programming. The power of what you can build. When I wrote my first useful program, I got goosebumps. 

{% highlight python %}
myList = []
with open('file.txt') as file:
  for line in file:
    myList += line.split(' ')
  for word in myList:
    if '@' in word:
      print word
{% endhighlight %}

I wrote the above script for grabbing email addresses in about 15 minutes. It saved me hours of work. I had been studying a bit of Python and Ruby, so I knew the basics about variables, arrays, loops, etc. And anything I didn't know--like how to open a file--I had Google.

Since then I've been scouring the internet to learn all things programming. From [Code School][code] to [TreeHouse][tree], [Stack Overflow][stack] to [Destroy All Software][DAS], there are hundreds of resources to help you learn software engineering. This blog will be about my journey along the way, perhaps with added unrelated ideas sprinkled in...like an ode to [Why's Poignant Guide to Ruby][why].

[why]:    http://mislav.uniqpath.com/poignant-guide/
[code]:   http://www.codeschool.com/
[tree]:   http://teamtreehouse.com/
[stack]:  http://stackoverflow.com/
[DAS]:    http://www.destroyallsoftware.com/