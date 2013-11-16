
Provides integration of Zurb Ink_ HTML email templates for Symfony2 projects.


Installation
============

Add marshmn/ink-bundle to composer.json

::

    "require": {
        "marshmn/ink-bundle": "~1.0@dev",
    }

Add MarshmnInkBundle to your AppKernel.php:

::

    // app/AppKernel.php
    public function registerBundles()
    {
        return array(
            // ...
            new Marshmn\InkBundle\MarshmnInkBundle(),
            // ...
        );
    }


Using The Templates
===================

The base templates provided in this bundle can be extended and then blocks overridden as desired.

The boilerplate template provides a skeleton email template:

::

    {% extends 'MarshmnInkBundle::boilerplate.html.twig' %}

    {% block bodycontent %}

        <p>Hello, World!</p>

    {% endblock %}


Alternatively, the basic template provides a more styled appearance:

::

    {% extends 'MarshmnInkBundle::basic.html.twig' %}

    {% block headerleftlabel %}My Project{% endblock %}

    {% block bodycontent %}

        <p>Hello, World!</p>

    {% endblock %}

    {% block calloutcontent %}

        <p>Call to action!</p>

    {% endblock %}



Take a look at the source templates to see what other blocks are available to be overridden.



.. _Ink:    http://zurb.com/ink
