# Unescaped multiline style reproduction (ssr forked from 'vue-cli-3-ssr (Beta)' )

Add ssr for vue-cli-3 app without using third paty plugins

## Running and Building

``` bash
# install dependencies
yarn install

# build all
yarn build

# Run ssr server in production mode
yarn start

# Serve with hot relod.
yarn serve

```

## Steps to reproduce

1. Serve with hot reload (yarn serve).
2. Visit route /example
3. Inspect page elements and notice how out of the 3 nested divs, only the parent's style is parsed and rendered correctly when in ssr. The other two are invalid because of the \n
4. Navigate to /home using the header link, and then back to /example using the browser's back button. Notice how now everything is rendered correctly.
5. In contrast, if you 'yarn build' & 'yarn start', everything is rendered correctly even in ssr.
