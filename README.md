# OPEN API functionality for Factom blockchain

Uses [OpenApi](https://docs.openapi.de-facto.pro/api-sdks) description from De Facto as basis for connecting to Factom blockchain. This repository contains a collection of utilities needed to work with Open API

- `factom-oapi-server` - folder with OpenAPI server re-implemented in Haskell, contains one-to-one translation from DeFacto's OpenApi server implementation with addition for several methods
- `factom-oapi-client` - folder with OpenAPi client for Haskell
- `factom-oapi-type`   - types that we share between Haskell server and Haskell client and keep clean code
- `factom-oapi-generated` - folder with additional clients that are generated from Haskell server implementation and Open APi definitions. Includeds `factom-elm-client.yaml`, `factom-purescript-client.yaml`

## Solution

- This system extends OpenApi specification from De Facto with addition of multiple endpoints. Our goal to have one-to-one mapping with RPC client which allow easier integrations with web-applications which usually follor REST pattern.

- We use Haskell because of brilliant type system that provide additional test layer by reducing specific classes of bugs that typial for other language. Type inference allows to detect incoherences at early stages and functional programming approaches gives ability to work easily with null-values and conditional responses..
