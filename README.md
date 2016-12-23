# UNI
A communication protocol for self-contained, platform-agnostic webviews



# SPECS

## Container

## Component

## Input

Input on a component is given by a

# Params

### `protocol` [<b>REQUIRED</b>] [<b>RESERVED</b>]

It's the protocol a component must use to communicate with its container

`http://path/to/my/view?protocol=guiabolso%3A%2F%2F`

The protocol is going to be prepended on the component's callback URI

### `callback`

A lower-camel-case word starting with 'on' defined by the following RegExp:

`on[A-Z][a-z]([A-Z][a-z]+)*`

Example: `onSubmit`

Usage Example:

`http://path/to/my/view?protocol=guiabolso%3A%2F%2F&onSubmit=submitHandler`

### `arbitrary`

Any arbitrary param a component can define as input, defined by the following RegExp:

`[a-z]([A-Z][a-z]+)*`

# State
`#some-state`

## Output
All the Output is made via `fetch` to a callback URI, wich is defined by:

`<callbackURI> ::= <protocol><callback>[?{<arbitrary>=<value>}&]`

`guiabolso://submitHandler?username=val1&password=val2`