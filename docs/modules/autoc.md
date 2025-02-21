# ~~autoc (auto complete)~~

NB: Yahoo decomissioned their autoc server sometime before 20 Nov 2021
(issue [#337](https://github.com/gadicc/node-yahoo-finance2/issues/337])).
Use [search](./search.md) instead (just like they do).


## Usage:

```js
import yahooFinance from 'yahoo-finance2';

const query = 'GOO';
const result = await yahooFinance.autoc(query, /* queryOptions */);

{
  Query: 'GOO',
  Result: [
    {
      symbol: 'GDRX',
      name: 'GoodRx Holdings, Inc.',
      exch: 'NMS',
      type: 'S',
      exchDisp: 'NASDAQ',
      typeDisp: 'Equity'
    },
    {
      symbol: 'GOOG',
      name: 'Alphabet Inc.',
      exch: 'NMS',
      type: 'S',
      exchDisp: 'NASDAQ',
      typeDisp: 'Equity'
    },
    {
      symbol: 'GOOGL',
      name: 'Alphabet Inc.',
      exch: 'NAS',
      type: 'S',
      exchDisp: 'NASDAQ',
      typeDisp: 'Equity'
    },
    // ....
}
```

See also: [search](./search.md).

## API

```js
await yahooFinance.autoc(query, queryOptions, moduleOptions);
```

### Query term

Symbol, company name, SEDOL, etc.

### Query Options

| Name          | Type      | Default    | Description                       |
| ------------- | ----------| ---------- | --------------------------------- |
| `region`      | number    | 1          |                                   |
| `lang`        | string    | "en"       |                                   |

### Module Options

See [Common Options](../README.md#common-options).
