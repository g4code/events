events
======

> events - [php](http://php.net) library

## Install

Via Composer

```sh
composer require g4/events
```

## Usage

```php
// Register event as an anonymous function
\G4\Events\PubSub::on('event_name', function($arg1, $arg2) { echo $arg1; echo $arg2; });

// Register event as a class method
\G4\Events\PubSub::on('event_name', [new \G4\Events\Test(), 'test']);

// Unregister all subscribers
\G4\Events\PubSub::clear();

// Unregister all subscribers based on event name
\G4\Events\PubSub::off('event_name');

// Unregister one single subscriber
\G4\Events\PubSub::off('event_name', [new \G4\Events\Test(), 'test']);

// Get all events and subscribers
\G4\Events\PubSub::getEvents();

// Check if event is registered
\G4\Events\PubSub::has('event_name');

// Check if subscriber is registered
\G4\Events\PubSub::has('event_name', [new \G4\Events\Test(), 'test']);

// Trigger event with arguments
\G4\Events\PubSub::trigger('event_name', [12345, 987]);

// Trigger event without arguments
\G4\Events\PubSub::trigger('event_name');
```

## Development

### Install dependencies

    $ make install

### Run tests

    $ make test

## License

(The MIT License)
see LICENSE file for details...
