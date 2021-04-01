# README

This repository reproduces
[issue #75](https://github.com/unabridged/motion/issues/75)
of the motion gem.

> When working with links that require the current domain, the domain is
> correctly loaded on the first load but will be replaced with
> http://example.org upon any page change.
>
> This can be reproduced simply by adding `<%= root_url %>` to a page and using
> a periodic timer to re-render the page.
>
> While absolute links are uncommon, they are used by ActiveStorage's direct
> upload. I have been able to avoid this issue by storing the URL to an instance
> variable in the controller and passing that value into the component so that
> it isn't being regenerated on page change.
