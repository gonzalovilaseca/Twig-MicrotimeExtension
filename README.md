Twig-MicrotimeExtension
=======================

This Twig extension formats a Unix microtime in a human readable format, it also calculates time between two microtimes.

Register the extension in symfony this way:
```
parameters:
    foo.twig.microtime.extension.class: Path\To\file\Twig\MicrotimeExtension
services:
    foo.twig.microtime.extension:
        class: %foo.twig.microtime.extension.class%
        tags:
            - { name: twig.extension }
```            
