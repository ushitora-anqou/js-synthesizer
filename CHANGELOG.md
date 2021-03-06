# Changelog

## v1.5.2

(This version has no bug-fixes and feature updates.)

- Update packages and build settings

## v1.5.1

- Fix to support iOS Safari that does not support `copyToChannel` on `AudioBuffer` (#2, thanks to @CreadDiscans)

## v1.5.0

- Remove `Fluid` namespace support (breaking change for initial user)
- Add `callFunction` method to `AudioWorkletNodeSynthesizer`
- Add some methods to `Synthesizer` such as `setChorus` and `setGenerator` (not add to `AudioWorkletNodeSynthesizer`)
  - To use those methods from audio worklet, load your script into audio worklet and use `callFunction`

## v1.4.1

- Fix to send 'unregister' event explicitly before unregistering client from Sequencer, to avoid access violation ('index out of range' error in JS)

## v1.4.0

- Add `SynthesizerSettings` object for initialization of synthesizer
  - The object can be specified for `init` method of `Synthesizer`, or `createAudioNode` method of `AudioWorkletNodeSynthesizer`.
- Add `setChannelType` method for Synthesizer (`ISynthesizer`)
- Add `removeAllEvents` / `removeAllEventsFromClient` methods for Sequencer (`ISequencer`)

## v1.3.0

- Rename package name to `js-synthesizer` (from `fluid-js`)
  - Old `fluid`-related files are currently supported, but will be removed in the future.
- The root namespace `Fluid` is changed to `JSSynth` for `js-synthesizer.js` file
  - The namespace `Fluid` is only available when using `fluid.js` (or files beginning with `fluid`), and the namespace `JSSynth` is only available when using `js-synthesizer.js` (or files beginning with `js-synthesizer`).

## v1.2.0

- Update libfluidsynth to 2.0.2 (using [fluidsynth-emscripten v2.0.2-em-fix1](https://github.com/jet2jet/fluidsynth-emscripten/releases/tag/v2.0.2-em-fix1))
- Add 'midiProgramSelect' API for synthesizer
- Add APIs for hooking MIDI events from player
- Add APIs for handling event data from sequencer (as 'sequencer client')
- Fix handling errors on the audio worklet

## v1.1.1

- Fix missing destination for sequencer

## v1.1.0

- Add APIs for player status and seekings (`seekPlayer` etc.)
- Add APIs for 'sequencer' processings
- Add 'waitForReady' API

## v1.0.0

- Initial version (using [fluidsynth-emscripten v2.0.1-em](https://github.com/jet2jet/fluidsynth-emscripten/releases/tag/v2.0.1-em))
