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

This does a partial match so this works:

```
bin/logreggator ui
```

And you can define multiple services, so this works too:

```
bin/logreggator internal-ui internal-api
```

## Examples

Get all api GET requests that are taking longer than a second to respond:

```
bin/logreggator api workflow | grep GET | egrep ' [0-9]{4,5}\.[0-9]{3} ms'
```
