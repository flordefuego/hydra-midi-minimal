# hydra-midi-minimal
extension for using webmidi with hydra

from:

[https://github.com/ojack/hydra-standalone/blob/master/docs/midi.md](https://github.com/ojack/hydra-standalone/blob/master/docs/midi.md)

#

[Example in hydra](https://hydra.ojack.xyz/?code=JTBBYXdhaXQlMjBsb2FkU2NyaXB0KCUyMmh0dHBzJTNBJTJGJTJGY2RuLmpzZGVsaXZyLm5ldCUyRmdoJTJGZmxvcmRlZnVlZ28lMkZoeWRyYS1taWRpLW1pbmltYWwlMkZtaWRpLW1pbmltYWwuanMlMjIpJTBBJTBBJTBBc2hhcGUoNCUyQzAuMSUyQzApLnNjYWxlKCgpJTNEJTNFY2MlNUI2NCU1RCUyQjAuNSklMEElMjAlMjAubXVsdChvc2MoMTAlMkMwLjElMkMoKSUzRCUzRWNjJTVCNjUlNUQpKSUwQSUyMCUyMC5vdXQoKQ%3D%3D)


```javascript
await loadScript("https://cdn.jsdelivr.net/gh/flordefuego/hydra-midi-minimal/midi-minimal.js")`
shape(4,0.1,0).scale(()=>cc[64]+0.5)
  .mult(osc(10,0.1,()=>cc[65]))
  .out()

```

in Orca for example
```
.......
.D...Cz
..!00..
.......
.D3..R.
.*!01..
.......
```

[Orca](https://github.com/hundredrabbits/Orca#midi-cc) uses web midi with `!` operator. Inputs('channel, 'knob, 'value). So `!00` is by default `CC64` and then it goes up, so  `CC65` is `!01` and so on...


