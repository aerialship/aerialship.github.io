---
    title: LightSaml
---


LightSaml Implements basic [SAML 2.0](http://saml.xml.org/saml-specifications) data model classes, serialization/deserialization
to/from xml with XML security and certificates support, and message encapsulations to bindings. It is covered with unit tests.

Download source from Github [LightSaml](https://github.com/aerialship/lightsaml) page.

Installation
------------

It is recommended you install LightSaml with composer

Add a requirement to your project composer.json

{% highlight json %}
# composer.json
{
    "require": {
        "aerialship/lightsaml": "dev-master"
    }
}
{% endhighlight %}

**Note**: *You should replace dev-master with concrete version.*

And then run from the command line composer update

{% highlight bash %}
$ composer.phar update aerialship/lightsaml
{% endhighlight %}

After that you will have LightSaml installed in your vendor directory.

