A benchmark command line tool for [limitd](https://github.com/auth0/limitd).

## Installation

```
npm install -g limitdb
```

## Usage

10k requests with concurrency level set to 10:

```
limitdctl --bucket ip --key 127.0.0.1 --take 1 -c 100 -n 100000
```

example results:

```
Doing 100000 TAKE operations with concurrency 100
┌────────────────┬──────────┐
│ Total time     │ 49598 ms │
├────────────────┼──────────┤
│ Errored        │ 0        │
├────────────────┼──────────┤
│ Conformant     │ 497      │
├────────────────┼──────────┤
│ Non Conformant │ 99503    │
├────────────────┼──────────┤
│ Mean           │ 49.56    │
├────────────────┼──────────┤
│ P50            │ 44.00    │
├────────────────┼──────────┤
│ P95            │ 79.00    │
├────────────────┼──────────┤
│ P97            │ 86.00    │
├────────────────┼──────────┤
│ Max            │ 489      │
├────────────────┼──────────┤
│ Min            │ 7        │
└────────────────┴──────────┘
```


## License

MIT 2015 - Auth0 Inc.