# test-github-token-rate-limit

Investigate the rate limit of `GITHUB_TOKEN`.

## Conclusion

- When a job is run, it does not consume the rate limit
- When a job uses action(s), it does not consume the rate limit
- `actions/checkout@v3` does not consume the rate limit

## Actions

### `actions/checkout@v3`

It does not consume the rate limit.

### `actions/setup-node@v3`

See https://github.com/int128/test-github-token-rate-limit/pull/5.
It does not consume the rate limit if a major version is given such as `16`.
However, it consumes 2 if a full version is given such as `16.15.1`.
