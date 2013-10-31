---
layout: post
title: LAMP install Ubuntu
description: "Brief summed up about the LAMP installation (on Ubuntu OS)."
modified: 2013-10-31
tags: [lamp brief]
image:
  feature: abstract-3.jpg
  credit: dargadgetz
  creditlink: http://www.dargadgetz.com/ios-7-abstract-wallpaper-pack-for-iphone-5-and-ipod-touch-retina/
comments: true
share: true
---

{% highlight css %}
sudo apt-get install lamp-server^
sudo apt-get install apache2-mpm-itk vim php5-curl
{% endhighlight %}

/etc/apache2/sites-available/site.loc =
{% highlight xml %}
<VirtualHost *:80>
  <IfModule mpm_itk_module>
    AssignUserId uvlek uvlek
  </IfModule>
  ServerAlias site.vh www.site.vh
  DocumentRoot /home/uvlek/www/site.vh
  <Directory /home/uvlek/www/site.vh/>
    AllowOverride All
  </Directory>
</VirtualHost>
{% endhighlight %}
 
/etc/apache2/conf.d/vhosts.conf =
{% highlight css %}
ServerName localhost
{% endhighlight %}

sudo vim /etc/hosts
+
{% highlight css %}
127.0.0.1 site.vh www.site.vh
{% endhighlight %}

REQU:
opencart
{% highlight css %}
sudo apt-get install php5-mcrypt php5-gd
{% endhighlight %}