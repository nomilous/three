Word: [component](https://github.com/component/component) provides a delicious capacity to build a more tightly focused clientside.

three
=====

three.js - base - NOT YET RECOMMENDED FOR CASUAL USE

* An attempt at dividing [three.js](https://github.com/mrdoob/three.js) into a workable set of [components](https://github.com/component/component)
* CherryPicking modules as needed, far from complete.
* **You WILL encounter missing dependancies**.
* You might like to contribute. I will be as receptive as I can afford to be. **Time is Valuable, Spare is Rare**.
* You could of course make you own component to include additional functionality. Keeping it to yourself might not be conducive to progress.
* Hopefully a clear outline of the necessary changes to push back upstream for a more component compatable three.js will accumulate below.
* Maintained from a Makefile in the [components branch of this fork of three.js](https://github.com/nomilous/three.js/tree/component/build/components)


### Usage

approx.

```

#
# (shell) install components and build
#

for COMPONENT in three three-scene three-camera three-webgl-renderer three-line three-particle; do
    component install nomilous/${COMPONENT}
done
component build


```

clientside.

```js


// assuming build.js has been loaded

require('three-webgl-renderer');
require('three-camera');
require('three-scene');
require('three-line');
require('three-particle');


// all of the above accumulated functionality into the instance returned below

THREE = require('three');

```


### Issues that would enjoy an upstream fix.

* extensive use of `instanceof`, specifically in shader and vertex program assembly in the renderers, but also generally
    * temporary fix while a full list accumulates: see `instanceof-U-later` in [nomilous/three-webgl-renderer](https://github.com/nomilous/three-webgl-renderer/blob/master/index.js)
