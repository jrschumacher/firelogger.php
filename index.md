---
title: FireLogger for PHP
subtitle: a sexy PHP logger console integrated into Firebug
layout: product
icon: /shared/img/firelogger4php-icon.png
repo: http://github.com/darwin/firelogger4php
support: http://github.com/darwin/firelogger4php/issues
downloadtitle: Install v0.1
download: https://addons.mozilla.org/en-US/firefox/addon/11090
downloadboxwidth: 210px
donate: https://addons.mozilla.org/en-US/firefox/addons/contribute/11090?source=addon-detail
subdownload: 
subdownloadlink:
mainshot: /shared/img/firelogger4php-mainshot.png
mainshotfull: /shared/img/firelogger4php-mainshot-full.png
overlaysx: 1120px
overlaysy: 986px
overlaycx: 25px
overlaycy: 10px
---


<div class="advertisement">
	<div class="plug">Recommended reading:</div>
	<a href="http://www.amazon.com/gp/product/0596009259?ie=UTF8&tag=firepython-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0596009259"><img border="0" src="/shared/img/amazon/41QbTFszYTL._SL110_.jpg"></a><img src="http://www.assoc-amazon.com/e/ir?t=firepython-20&l=as2&o=1&a=0596009259" width="1" height="1" border="0" alt="" style="border:none !important; margin:0px !important;" />
	
	<a href="http://www.amazon.com/gp/product/0596158068?ie=UTF8&tag=firepython-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0596158068"><img border="0" src="/shared/img/amazon/41Mu5RWG-1L._SL110_.jpg"></a><img src="http://www.assoc-amazon.com/e/ir?t=firepython-20&l=as2&o=1&a=0596158068" width="1" height="1" border="0" alt="" style="border:none !important; margin:0px !important;" />

	<a href="http://www.amazon.com/gp/product/0596007973?ie=UTF8&tag=firepython-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0596007973"><img border="0" src="/shared/img/amazon/41S-nPeF89L._SL110_.jpg"></a><img src="http://www.assoc-amazon.com/e/ir?t=firepython-20&l=as2&o=1&a=0596007973" width="1" height="1" border="0" alt="" style="border:none !important; margin:0px !important;" />
	
	<a href="http://www.amazon.com/gp/product/1430210478?ie=UTF8&tag=firepython-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=1430210478"><img border="0" src="/shared/img/amazon/516STCBRnOL._SL110_.jpg"></a><img src="http://www.assoc-amazon.com/e/ir?t=firepython-20&l=as2&o=1&a=1430210478" width="1" height="1" border="0" alt="" style="border:none !important; margin:0px !important;" />
	
	<a href="http://www.amazon.com/gp/product/059652272X?ie=UTF8&tag=firepython-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=059652272X"><img border="0" src="/shared/img/amazon/513CiT5BtYL._SL110_.jpg"></a><img src="http://www.assoc-amazon.com/e/ir?t=firepython-20&l=as2&o=1&a=059652272X" width="1" height="1" border="0" alt="" style="border:none !important; margin:0px !important;" />
	
	<div class="offer"><a href="mailto:antonin@binaryage.com">advertise here</a></div>
</div>
<script type="text/javascript" src="http://www.assoc-amazon.com/s/link-enhancer?tag=firepython-20&o=1">
</script>

## Features

* Your logging messages are displayed right under your fingerprints in Firebug
* Support for rich-text logging (logged objects are sent as JSON object, you may drill down their structure)
* Support for advanced features:
  * open in Text Editor integration
  * production paths remapping
  * and more ...

### Compatibility

* **Version 0.1** works with:
  * beta Firebug 1.4 + Firefox 3.0.x or Firefox 3.5
  * does not work with Firebug 1.3 and older!

## Installation

You definitely need [Firebug 1.4 or higher][firebug]. You also have to install Firefox Addon which is called [FireLogger][firelogger].

#### Firefox Addon
Preferred way is to [install this firefox extension][firelogger] via addons.mozilla.com.

#### PHP Library

    require 'firelogger.php';
    flog("Hello world!");

## FAQ

#### What is the difference between FireLogger and [FirePHP](http://www.firephp.org/)?
> Initially I've written [FireLogger for Python](http://firepython.binaryage.com) because I was doing some Google App Engine development. Recently I was asked to do some PHP development. I've tried FirePHP, it worked for me, but it wasn't "pixel perfect" to fit my personal taste :-) I'm a javascript guy quite opinionated about tools. I wanted flexible dirty logging function which is capable of eating whatever I throw into it (like firebug's console.log). I also prefer to have server-side logger console separated from javascript console in Firebug. I prefer reusing firebug's internal components for variables inspection. FireLogger has the same look&feel as javascript console (you can drill down watches firebug-way, same fonts and colors, etc.). FireLogger has also some advanced features which may be handy (password protection, "open in text editor" and production paths remapping).

#### Clicking on source-file links in Logger panel does nothing. How can I open trace-back sources in TextMate?
> Go to Firebug Menu -> Open With Editor -> Configure editors ... like this: ![TextMate hint][textmate-hint]

#### I was unable to download/install FireLogger extension from addons.mozilla.org. Can you package latest version for me?
> Some people reported this problem too. You may [try workaround][workaround].

#### When I start Firefox and page loads I don't see any log records, what is wrong?
> First page content was probably loaded from cache. Refresh your page and you should be ok.

#### My page does multiple AJAX requests to the same URL, I see logs for the first response, but not for others. Am I missing something?
> There is a bug in Firebug 1.4, it calls onResponse multiple times under some circumstances. That was very annoying, so I did a HACK and test for URL uniqueness in FireLogger. This will unfortunately filter out your multiple AJAX requests. Let's hope for fixes on Firebug side.

## History

* **v0.1** (17.08.2009)
  * [[darwin][darwin]] initial implementation, supports basic logging

## Links

### Sites

* **[FirePython](http://firepython.binaryage.com)** - original logging project

### Also thanks to

* **[Joe Hewitt, John J. Barton, Jan Odvarko and others in Firebug working group][firebug-team]** - without these guys, the web wouldn't look like today.
* **[Christoph Dorn and FirePHP contributors][firephp-authors]** - a lot of inspiration, good work mates!

[firebug]: https://addons.mozilla.org/en-US/firefox/addon/1843
[firelogger]: https://addons.mozilla.org/en-US/firefox/addon/11090
[workaround]: http://getsatisfaction.com/xrefresh/topics/unable_to_download_rainbow_for_firebug
[darwin]:http://github.com/darwin
[firebug-team]:http://getfirebug.com/workingGroup
[firephp-authors]:http://www.christophdorn.com/
[textmate-hint]:http://cloud.github.com/downloads/darwin/firepython/TextMateWithFirePython.png
