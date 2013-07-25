---
layout: post
title:  "Coding Connections"
date:   2013-07-25 15:15:00
categories: clean simple code
---
Coding is all about connections. In fact, that's the hardest part. Making sure the various elements are accurately connected, making sure everyone's talking to each other. The actual computation or logistics of the program can be rather simple.

Take the site-reading code below, for example. Most of the magic happens with the `require "open-uri"` on line one. This is code that's already written for you and widely used in Ruby. [OpenURI][openURI] essentially allows the computer to open a web page and read it like a file. Now that this part is done, and the connection from your terminal to a web page is made, the rest is easy. 

{% highlight ruby %}
require "open-uri"

def read_a_url
  print "Count the images from a url. Enter the domain address http://"
  url = "http://" + gets.chomp

  page = open(url).read
  tags = page.scan("<img")

  puts "The site #{url} has #{tags.length} img tags"
end

read_a_url()
{% endhighlight %}

We ask the user to enter a domain address with the print command. We run `gets` to store the user's input and `chomp` to remove the last character (in this case, a new line "\n"). We store this input (or create a pointer to its location in memory, if you want to get technical) into url. We then open the url, read it and store it as the page variable, where we run the `scan` method passing in the `"<img"` parameter and storing this to the tags variable. Finally, print the info to the screen with puts, calling the `length` method on tags.

Code like this is why I (like many others, I imagine) fell in love with Ruby. Methods are simple and easy to understand. Do you want the computer to read a file? Call the read method. What's the length of a variable? Call the length method. Content may be king in the world of marketing, but in programming, simplicity is king.

If you like this example, check out [The Bastards Book of Ruby][bbRuby], where I first discovered a slightly different version that I tweaked for this post. If you've never visited this site, I highly recommend it. The Bastards Book is an exhaustive and excellent resource of all things Ruby.

[openURI]:    http://www.ruby-doc.org/stdlib-2.0/libdoc/open-uri/rdoc/OpenURI.html
[bbRuby]:     http://ruby.bastardsbook.com/chapters/methods/