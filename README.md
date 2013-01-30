# What this is for?

Rails engine to log from Client side (Browser) javascript to server log file. Makes a global javascript variable available, 'jsLogger', which provides a variety of safe logging functions e.g. jsLogger.debug(), jsLogger.error().

There are 5 levels of logging: debug, info, warn, error and fatal.

## Installation

Add this line to your application's Gemfile:

    gem 'js-logger'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install js-logger

## Usage

Includes a generator, simply execute following command in your rails project root. It inserts the required routes and javascript files.

    rails g js_logger

### Logging a message

    jsLogger.info("simple info message");
    jsLogger.warn("a warning");

### Log Error

    try {
        throw new Error('unhandled exception');
    }
    catch (e) {
        jsLogger.fatal(e);
    }

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

## License
MIT License

Copyright (c) 2013 Girish Sonawane (girish dot sonawane at gmail dot com)

