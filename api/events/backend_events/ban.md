# Ban message

Event passed when a person is banned

**Note**: the ban duration offers you the following three options

* **h**: Banned for an hour
* **d**: Banned for a day
* **f**: Banned for ever

### Example

```js
{
    "a": "ban",         // Event name
    "p": {
        "t": "ban",
        "d": "x",       // Duration
        "r": -1         // Reason
    },

    "s": "dashboard"
}
```
### Real life example
```js
{
    "a": "ban",         // Event name
    "p": {
        "t": "ban",
        "d": "h",       // Duration
        "r": 1          // Reason
    },

    "s": "dashboard"
}
```

