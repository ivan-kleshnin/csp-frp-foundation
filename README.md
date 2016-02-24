# CSP as FRP foundation

Sketches.

## Content

### [01. consume / broadcast](./01.consume.broadcast.md)

Consume values from input channel. Broadcast values from input channel.

### [02. tap](./02.tap.md)

Produce side effects from input channel without values being consumed.

### [03. sleep](./03.sleep.md)

Freeze task for defined time.

### [04. drawEvery / callEvery / repeatEvery](./04.drawEvery.callEvery.repeatEvery.md)

Generate sequential values over time.

### [05. merge](./05.merge.md)

Merge values from input channels into output channel.

## Notes

Every time your project is promise-based (async-await is) – don't forget to add something like

```js
// backend only: need condition for isomorphic app
process.on("unhandledRejection", function (reason, p) {
  throw reason;
});
```

into app root file. Blame NodeJS devs for that.
