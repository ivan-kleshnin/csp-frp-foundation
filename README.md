# CSP as FRP foundation

Sketches.

## Content

### [01. consume / broadcast](./01.consume.broadcast.md)

Consume values from input channel. Broadcast values from input channel.

### [02. tap](./02.tap.md)

Produce side effects from input channel without values being consumed.

### [03. sleep](./03.sleep.md)

Pause task for defined time.

### [04. drawEvery / callEvery / repeatEvery](./04.drawEvery.callEvery.repeatEvery.md)

Generate sequential values over time.

### [05. merge](./05.merge.md)

Merge values from input channels into output channel.

### [06. delay](./06.delay.md)

Delay every value from input channel for defined time.

### [07. lift](./07.lift.md)

Apply function over input streams. First call will be delayed until all input channels yield.

### [08. map / filter / scan](./07.map.filter.scan.md)

Classic functional triad.

## Notes

Every time your project is promise-based (async-await is) – don't forget to add something like

```js
// backend only: need condition for isomorphic app
process.on("unhandledRejection", function (reason, p) {
  throw reason;
});
```

into app root file. Blame NodeJS devs for that.
