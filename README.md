# semann adapters

> Start compatible adapters to _[semann](https://netresearch.github.io/semann/)_, your content enhancer.

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

## Contribute

1. Fork it
2. Create your feature branch (git checkout -b my-new-feature)
3. Commit your changes (git commit -am 'Add some feature')
4. Push to the branch (git push origin my-new-feature)
5. Create new Pull Request

### Issues

Please report issues to [ticket system](https://github.com/netresearch/semann-adapters/issues). 
Pull requests are welcome here!
