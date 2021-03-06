# lita-ignore-me

*lita-ignore-me* is a Lita extension that allows a user to tell the robot that he or she wishes to be ignored unless addressing the robot directly. This means that routes that are triggered that are not commands are not executed.

## Installation

Add lita-ignore-me to your Lita plugin's gemspec:

``` ruby
spec.add_runtime_dependency "lita-ignore-me"
```

## Usage

There is no additional configuration necessary. There are two commands added for a user to manage whether the robot will listen to or ignore that user in the current room: `ignore me` and `listen to me.

Assuming there is some handler that echoes messages that start with 'echo' installed and configured, a conversation might look like this:

```
Chad: echo I don't like to be echoed.
Lita: I don't like to be echoed.
Chad: @Lita: ignore me
Lita: Okay Chad, I'll ignore you in #channel unless you address me directly.
Chad: echo I don't like to be echoed.
Chad: lita help
Lita: *prints help*
Chad: @Lita: listen to me
Lita: Okay Chad, I'm listening.
Chad: echo I expect to be echoed.
Lita: I expect to be echoed.
```

## License

[MIT](https://opensource.org/licenses/MIT)
