Word: [component](https://github.com/component/component) provides a delicious capacity to build a more tightly focused clientside.

three
=====

three.js - base - NOT YET RECOMMENDED FOR CASUAL USE

* An attempt at dividing [three.js](https://github.com/mrdoob/three.js) into a workable set of [components](https://github.com/component/component)
* CherryPicking modules as needed, far from complete.
* **You WILL encounter missing dependancies**.
* You might like to contribute. I will be as receptive as I can afford to be. **Time is Valuable, Spare is Rare**.
* Maintained from a Makefile in the [components branch of this fork of three.js](https://github.com/nomilous/three.js/tree/component/build/components)


Usage
-----

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

#
# assuming build.js has been loaded
#

require('three-webgl-renderer');
require('three-camera');
require('three-scene');
require('three-line');
require('three-particle');

#
# all of the above accumulated functionality into the instance returned below
#

THREE = require('three');

```
