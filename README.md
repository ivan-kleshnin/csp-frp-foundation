# CSP as FRP foundation

Sketches.

## Notes

Every time your project is promise-based (async-await is) – don't forget to add something like

```js
process.on("unhandledRejection", function (reason, p) {
  throw reason;
});
```

into app root file. Blame NodeJS devs for that.

## [01. consume / broadcast](./01.consume.broadcast.md)

Consume values from input channel. Broadcast values from input channel.

## [02. tap](./02.tap.md)

Produce side effects from input channel without values being consumed.

## [03. sleep](./03.sleep.md)

Freeze task for defined time.

## [04. drawEvery / callEvery](./04.drawEvery.callEvery.md)

Generate sequential values over time.
