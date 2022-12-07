# Condensed Game Audio

I wanted small audio files for my games. Games should have the ability to have both sound effects and music playing at the same time. TIC80 has a fairly compact audio format, only I found it beyond what I had time to do to port it to the web, being that I would have to rip out the rest of the engine, and the format was designed to interact with internal programming languages and the rest of the TIC80 memory structure.

Thus, this project is my attempt at doing a compact audio format that like TIC80 can do sound effects, and music. Sort of similar to mod formats, but only built out of editable single waves, and instruments (sound effects) can be built out of a combination of those waves instead of only a single one.

The format is focused on sound, wave, and sfx reuse so as to be as small as reasonable.

I hope that the audio player itself is small. There's a mod player available that is 40KB and so that is my target size for this code once compiled to wasm, and including necessary javascript linking code.

The reason this code is in Rust, instead of JavaScript is that Mozilla's documentation strongly implied that WebAssembly should be used for AudioWorklets. The reason Rust is used instead of my more familar C++/C is because this will involve a lot of buffer management and that's the exact kind of thing that leads to vulnerabilities in C code. I don't want crashes, and I don't want vulnerabilities if people use this code from a native application.

I do not know if I will succeed, but I will document my progress here.

## Compile

``` shell
rustc cga.rs
```

## Run

```shell
./cga
```
