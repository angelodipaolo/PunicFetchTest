# PunicFetchTest

Sample for reproducing a bug in `punic fetch` using Punic version 0.2.2 with Python version 2.7.12.

## Steps to Reproduce

- Clone this repo
- Run `punic resolve`
- Run `punic fetch`

## Result

Punic fails to checkout the contents of the dependencies into the Carthage/Checkout directory. An empty Carthage/Builds directory is created (which is expected since it should not build the dependencies) but the contents of the dependencies are not checked out.

## Expected

Punic should checkout the contents of the dependencies into the Carthage/Checkout directory.

It's worth noting that this same behavior is also reproducible by running `punic resolve --fetch`.
