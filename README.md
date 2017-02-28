# semann adapters

> Start compatible adapters to _semann_, your content enhancer.

## Included adapter

Currently only [Stanbol](https://stanbol.apache.org/) is included.

## Usage

``` bash
docker-compose up -d
```

### Configuration

``` javascript
new Semann(
    {
        target: document.querySelector('#semannContainer'),
        app: {
            config: {
                connectors: {
                    stanbol: {
                        adapter: 'stanbol',
                        url: 'https://your-adapters.io:9988',
                        features: {
                            chain: [
                                'dbpedia-disambiguation',
                                'dbpedia-fst-linking',
                                'dbpedia-proper-noun',
                                'dbpedia-spotlight',
                                'language'
                            ]
                        }
                    }
                }
            }
        }
    }
)
```

For detailed explanation on how things work, checkout the [semann guide](https://github.com/netresearch/semann).
