# Pushover

This gem provides a CLI and an API interface to http://pushover.net.

## Installation

To install:

  % gem install pushover

To use inside of an application, add this to the your gemfile:

  % gem 'pushover'

and run bundle to make it available:

  % bundle

## Usage

To get help:

    pushover help

supply a token:

    pushover --token '...'

supply an application key:

    pushover --app_key '...'

## API

```ruby
require 'pushover'
```

### Create a message

```ruby
message = Pushover.create {
  user: '...',
  token: '...',
  message: '...'
}
```

### Send the message

```ruby
  response = message.send
```

### Response

- The response will always include `status` and `request`.
- When set, it will also include `errors` and `receipt`.

```ruby
  response.status
  response.request
```


## Contributing

1. Fork it
2. Switch to development (`git checkout developtment`)
3. Create your feature branch (`git checkout -b my-new-feature`)
4. Commit your changes (`git commit -am 'Added some feature'`)
5. Push to the branch (`git push origin my-new-feature`)
6. Create new Pull Request against `development`
