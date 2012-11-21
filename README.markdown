# Sparcet Aside for Octopress


Use [Sparcet](http://www.sparcd.com)?  Want to show off your recent sparcets on your Octopress blog?

I created this simple plug for the purposes of displaying recent sparcets that were given to me.

Sparcet has a public api posted [HERE](https://github.com/sparcedge/Sparcet-Public) which is what I used to access the public feeds from the Sparc Platform.

If you haven't heard of sparcets, they are a new way to recognize your peers/coworkers. If your organization or company isn't using [Sparcet](http://www.sparcd.com), you should check them out!

You can view it in action on my [blog](http://blog.hellocalvin.com)

## Installation

### 1. Choose which version of the aside you want to use.  (They both use jquery, I just used jQuery.noConflict() in the ender one).

### 2. I've created the path to the relevant directory in Octopress to put the sidebar file, simply navigate to that path in your setup and paste it in there.
```/source/_includes/asides/```

### 3. In your ```_config.yml```, add the file reference in default_asides, or if you only want it to appear in certain places,blog_index_asides, page_asides, or post_asides.

Example:

```
default_asides: [asides/sparcet.html, asides/github.html, asides/twitter.html, asides/delicious.html, asides/pinboard.html, asides/googleplus.html]
```

### 4. Now that you have added the aside sparcet.html, you'll need to finish your ```_config.yml``` to include the information about your sparcets

```
# Sparcet
sparcet_user: YOUR_USER_ID           # This is a unique ID, not a username - To find yours: http://{tenant}.sparcet.com/api/users?q={email or partial string}
sparcet_count: HOW_MANY_TO_LIST         # How many sparcets do you want to list
sparcet_tenant: YOUR_ORGANIZATION        # Specific Tenant (eg. sparc)

```
Please know it's not intuitive to get your [Sparcet](http://www.sparcd.com) user ID and you'll need to query it (for now) using this url pattern:

```http://{tenant}.sparcet.com/api/users?q={email or partial string}```

If your organization does not have public sparcets, then this api will not render anything.
---------------------------------------


License
-------

The MIT License (MIT)

Copyright (c) 2012 Calvin Webster

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.