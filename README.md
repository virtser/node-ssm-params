# ssm-params

Obtain parameters from AWS SSM Parameter Store.

## Installation

```
npm i ssm-params aws-sdk -S
```

## API

### ssmToObj(options, callback)

- `options`
    - If this is a string, it is equivalent to specify `options.prefix` only.
- `options.prefix`
    - A prefix of parameter names to obtain parameters.
- `options.target`
    - A target object that is set values of obtained parameters.
    - Default: `{}`
- `callback(err, target)`
    - A callback which is called when obtaining parameters have finished,
      or an error occurs.
    - If an error does not occur, `target` is passed `options.target`.

### ssmToEnv(prefix, callback)

This is equivalent to call `ssmToObj` with specifying `process.env` to a target.

- `prefix`
    - This is equivalent to `options.prefix` of `ssmToObj`.
- `callback(err, target)`
    - This is equivalent to `callback` of `ssmToObj`.

## License

MIT