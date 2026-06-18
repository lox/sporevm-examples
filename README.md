# SporeVM Examples

Examples for running real application workloads with
[SporeVM](https://github.com/buildkite/sporevm).

## Examples

- [Rails/Postgres RSpec fan-out](rails/README.md): build a Rails/Postgres test
  image with Docker buildx, import it into SporeVM's local rootfs cache, warm the
  VM once, capture it, fork child spores, and run RSpec shards in parallel.

## SporeVM Checkout

The scripts default to a sibling SporeVM checkout:

```bash
git clone https://github.com/buildkite/sporevm ../sporevm
```

You can also point at another checkout or binary:

```bash
SPOREVM_REPO=/path/to/sporevm bash rails/bin/fanout-rspec
SPORE_BIN=/path/to/spore bash rails/bin/fanout-rspec --no-build
```

