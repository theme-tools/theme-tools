# Theme Tools by Basalt

> Flexible, un-opinionated tools for front end development.

This is a monorepo of a lot of awesome stuff. Everything in `packages/` can be `npm install`-ed by itself - and each of those packages is focused on solving a single need in front end web development, like needing to work with CSS for example. As many know, there's so much more to a good setup than just compiling Scss to CSS: linting, docs, compressing, handling vendor prefixes, managing file assets CSS needs like font files & images - not to mention a watch task for each of those. And that's what Theme Tools plugins do: they solve a collection of challenges to effective tooling around a single need. These examples are just around `plugin-sass`; there's several others as well and they all can be combined in different ways depending on the needs of the specific project - use as many or as little as you'd like - even in your pre-existing setup.

See the `packages/` folder for the individual npm modules.

See the `examples/` folder for how it can all come together.

Each take a config object and returns an object containing functions that it can run, like a css compile, or watch css to compile. No plugins contain `gulp.task()`.

# Contributing

## Dev Setup

This uses [`lerna` for monorepo setup](https://github.com/lerna/lerna).

```bash
npm install
npm run bootstrap # this is `lerna bootstrap`
```

---

## Why is this a monorepo?

> Inspired by Babel. Thanks!

The tool for managing the monorepo is [Lerna](https://github.com/lerna/lerna)

Juggling a multimodule project over multiple repos is like trying to teach a newborn baby how to ride a bike.

This is quite taboo but let's look at the pros and cons:

**Pros:**

 * Single lint, build, test and release process.
 * Easy to coordinate changes across modules.
 * Single place to report issues.
 * Easier to setup a development environment.
 * Tests across modules are ran together which finds bugs that touch multiple modules easier.

**Cons:**

 * Codebase looks more intimidating.
 * Repo is bigger in size.
 * ???

## This is dumb! Nobody in open source does this!

[Babel](https://github.com/babel/babel/tree/master/packages), [React](https://github.com/facebook/react/tree/master/packages), [Meteor](https://github.com/meteor/meteor/tree/devel/packages), and [Ember](https://github.com/emberjs/ember.js/tree/master/packages), among others, do this.

## Previous discussion

- [Dan Luu](http://danluu.com/monorepo/)
- [Gregory](http://gregoryszorc.com/blog/2014/09/09/on-monolithic-repositories/)
- [Szorc](http://gregoryszorc.com/blog/2015/02/17/lost-productivity-due-to-non-unified-repositories/)
- [Face](https://www.youtube.com/watch?v=X0VH78ye4yY)[book](https://code.facebook.com/posts/218678814984400/scaling-mercurial-at-facebook/)
- [Benjamin Pollack](http://bitquabit.com/post/unorthodocs-abandon-your-dvcs-and-return-to-sanity/)
- [Benjamin Eberlei](https://qafoo.com/resources/presentations/froscon_2015/monorepos.html)
- [Simon Stewart](http://blog.rocketpoweredjetpants.com/2015/04/monorepo-one-source-code-repository-to.html)
- [Digital Ocean](https://www.digitalocean.com/company/blog/taming-your-go-dependencies/)
- [Google](http://www.infoq.com/presentations/Development-at-Google), [another](https://www.youtube.com/watch?v=W71BTkUbdqE)
- [Twitter](https://www.youtube.com/watch?v=bjh4DHuOf4E)
- [thedufer](http://www.reddit.com/r/programming/comments/1unehr/scaling_mercurial_at_facebook/cek9nkq)
- [Paul Hammant](http://paulhammant.com/categories.html#Trunk_Based_Development)
- [Exponent](https://blog.getexponent.com/universe-exponents-code-base-f12fa236b8e#.9dj8a82be)
