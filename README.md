# ASL log aggregator

Allows streaming the logs across multiple pods.

## Usage

Get on the right VPN.

### Prod:

```
bin/logreggator
```

### Notprod

```
bin/logreggator --env dev|preprod
```

### Options

To filter to only matching services:

```
bin/logreggator public-ui
```

This does a partial match so you this works:

```
bin/logreggator ui
```

And you can define multiple services, so this works too:

```
bin/logreggator internal-ui internal-api
```
