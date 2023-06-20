# Reuron

Reuron is a web-first neural network simulator.

It provides the same functionality as [NEURON](https://www.neuron.yale.edu/neuron/), [BRIAN](https://briansimulator.org/) and [PyNN](https://neuralensemble.org/PyNN/), but with a focus on web compatibliity over all else.

The web-first mindset means:

 - Reuron can be run without installing anything. Just go to https://reuron.io .
 - You can share working reuron models by sending a single URL.
 - Model configurations are hyperlinked and encourage remixing.

## Project organization

### [reuron](https://github.com/reuron/reuron)

The simulation engine, which is a (Rust)[https://www.rust-lang.org/] application
written in the [Bevy](https://bevyengine.org/) game engine.

### [reuron-io](https://github.com/reuron/reuron-io)

A web server running at https://reuron.io . It hosts the static assets of the
simulator, and an endpoint used for interpreting configuration files that
specify neural networks.

See [the repository](https://github.com/reuron/reuron.io)'s documentation for a
more thorough description of these APIs.

### [reuron-lib](https://github.com/reuron/reuron-lib)

A collection of configuration snippets used for building out networks, for
example standard
[channels](https://github.com/reuron/reuron-lib/blob/main/channels.ffg) and
[membrane types](https://github.com/reuron/reuron-lib/blob/main/membranes.ffg),
and an example
[scene](https://github.com/reuron/reuron-lib/blob/main/scene.ffg).
