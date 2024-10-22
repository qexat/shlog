# shlog

A simple Bash utility to log useful messages.

## Commands

- shask
- sherror
- shinfo
- shnote
- shsucceed
- shwarn

## Examples

```sh
$ sherror "failed to open the file"
ERROR: failed to open the file
$ shinfo "foo" "a new update is available"
INFO: foo: a new update is available
$ shlog note "bar" "do ré mi fa sol la si"
NOTE: bar: do ré mi fa sol la si
```

Colors are present in the output but not visible in the examples.

## Usage

```sh
shlog <kind> [origin] <message>
<command> [origin] <message>
```

### Arguments

#### kind

The type of log to print.
(Possible choices are: error, success, warning, info, question, note)

#### origin

Where the log comes from. Must be a valid identifier.

#### message

The logging message.

### Exit codes

#### 2

- The number of arguments is less than 2

#### 1

- The kind is invalid (not from the possible choices)
- The origin is not a valid identifier
