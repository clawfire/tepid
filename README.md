# Tepid

Tepid is a lightweight typography theme, with many colors in orange tone. It's a Casper (default Ghost theme) fork, so if you like Ghost there's a big chance that you will love Tepid. It's a [Ghost](http://ghost.org) theme created for my [Blog](http://clawfire.net).

This project is a fork originaly made by [wcsantos](http://wcsantos.com) .

## Comment system : Livefyre
[Livefyre](http://livefyre.com) is a free comment system that you can use for you blog. You can register for the free comment produit on their webiste and edit the code found on `post.hbs` line `128` to put your own `siteId`.

```
siteId: "yourIdHere",
```

### Import from wordpress
As you can see into my code, I previously use wordpress for my blog. And I use Livefyre also. They have a good [wordpress plugin]() to do so. But the problem is that Ghost doesn't respect the wordpress `post_id` when it import your file exported from the [Ghost Export tool for wordpress](). So I had to match it manually. The trick is kind of easy : 

1. Change the date of your migration from wordpress line `81` : `var migration_wordpress  = moment('2013-12-31');` It's a date with the format `YYYY-MM-JJ`
2. If, like me, you start to already use livefyre by the past, without this theme, please also change the line `82`: `var migration_new_articleID = moment('2014-09-28');` with the date of using the theme for the first time ( in fact publishing an article with this theme used ). **If you don't please set the same date than previously**

### No import from wordpress
If you don't import anything from wordpress, you don't need my hack. In the future i'll try to move this change on a dedicated branch but before it will happen, please remove line `81` to `123` **without** the line `116`. Keep only this line from this line range. You don't need all this javascript madness just write because of arogance of some Ghost devs.

## Copyright & License

Copyright (C) 2013 Ghost Foundation - Released under the MIT License.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
