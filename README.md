# AppSignal Documentation

This repository contains the source for the [AppSignal documentation
website][docs].

- [AppSignal.com website][appsignal]
- [Documentation][docs]
- [Support][contact]

## Setup

Run the following commands:

```sh
git submodule init
git submodule update
```

## Usage

```sh
bundle install
bundle exec middleman
```

Open the browser at [localhost:4567](http://localhost:4567/) and click around.

## Deployment

```sh
bundle exec rake build_deploy
```

## Content

### Markdown customizations

To render notices we've added a custom markdown tag. Use it like so:

```markdown
!> This is a warning!
-> This is a notice!

# I'm a heading
#^prefix I'm a heading
```

Which will render the following:

```html
<div class="warning">
  <p>This is a warning!</p>
</div>
<div class="notice">
  <p>This is a notice!</p>
</div>

<h1><span class="anchor" id="im-a-heading"></span><a href="#im-a-heading">I'm a heading</a></h1>
<h1><span class="anchor" id="prefix-im-a-heading"></span><a href="#prefix-im-a-heading">I'm a heading</a></h1>
```

For more information (and code) about these customizations, please see the
[`appsignal_markdown.rb`](lib/appsignal_markdown.rb) file.

## Contributing

Thinking of contributing to our documentation? Awesome! 🚀

Please follow our [Contributing guide][contributing-guide] in our
documentation.

Also, we would be very happy to send you Stroopwaffles. Have look at everyone
we send a package to so far on our [Stroopwaffles page][waffles-page].

[appsignal]: https://appsignal.com
[contact]: mailto:support@appsignal.com
[waffles-page]: https://appsignal.com/waffles
[docs]: https://docs.appsignal.com
[contributing-guide]: https://docs.appsignal.com/contributing
