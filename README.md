# UNI
A communication protocol for self-contained, platform-agnostic webviews



# SPECS

## container

## Component

## Input

Input on a component is given by a

# Params

### `protocol` [<b>REQUIRED</b>] [<b>RESERVED</b>]

It's the protocol a component must use to communicate with its container

Example: `guiabolso://`

The protocol is going to be prepended on the component's callback URI

### callback params 

`A lower-camel-case word starting with 'on'`

If a param starts with `on` then it's assumed it is a event handler.

Example: `onSubmit`

`http://path/to/my/view?param1=value1&param2=value&onChangeCallback=changeHandler&protocol=guiabolso%3A%2F%2F`

### arbitrary params

# State
`#some-state`

## Output

`guiabolso://changeHandler?value=value1`