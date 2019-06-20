# JUST EAT Partner API Specification
[![Build Status](https://travis-ci.org/justeat/partnerapi-docs.svg?branch=master)](https://travis-ci.org/justeat/partnerapi-docs)

Documentation: https://justeat.github.io/partnerapi-docs/

Preview (when using a branch) `[branch]`: https://justeat.github.io/partnerapi-docs/preview/[branch]

**Warning:**  Above link is updated only after Travis CI finishes deployment


## Working on specification

### Install

1. Install [Node JS](https://nodejs.org/)
2. Clone repo and `cd`
    + Run `npm install`
3. Newer versions of npm will fail with an error similar to:

```javascript
 gulp[11376]: src\node_contextify.cc:629: Assertion `args[1]->IsString()' failed.
 1: node::DecodeWrite
 2: node::DecodeWrite
 3: uv_loop_fork
 4: v8::internal::interpreter::BytecodeDecoder::Decode
 5: v8::internal::RegExpImpl::Exec
 6: v8::internal::RegExpImpl::Exec
 7: v8::internal::RegExpImpl::Exec
 8: 00000384E1284281
 ```

+ To fix this run `npm install natives`


### Usage

1. Run `npm start`
2. Checkout console output to see where local server is started. You can use all [links](#links) (except `preview`) by replacing https://justeat.github.io/partnerapi-docs/ with url from the message: `Server started <url>`
3. Make changes using your favorite editor
4. All changes are immediately propagated to your local server, moreover all documentation pages will be automagically refreshed in a browser after each change
5. Once you finish with the changes you can run tests using: `npm test`
6. Share you changes with the rest of the world by pushing to GitHub :smile:

### The Framework

This documentation is built using 
 - [ReDoc](https://github.com/Rebilly/ReDoc) as the site template (see web/index.html for the version being used
 - [Yeoman Generator for OpenAPI](/generator-openapi-repo) which allows us to store the OpenAPI spec as lots of separate YAML files and then combine and genreate OpenAPI json.  This makes the spec easier to edit, as it's not one huge file! 


