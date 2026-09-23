# TurboQOA

From scrtch, realtime [Quite Ok Audio](https://qoaformat.org/) codec with streaming support written in pure C. I wrote this thing because I don't want to interdace with the complexity of OGG/OPUS and I don't care that much about audio quanlity and/or compression ratio. QOA's 5x compression is good enough.

## How to compile and use it
```bash
mkdir build
cd build
cmake ..
make
```
Tools work with PCM files:
```bash
$ ./encode         
Usage: ./encode <input.pcm> [<output.qoa>]
$ ./decode   
Usage: ./decode <input.qoa> [<output.pcm>]
```

## How to read QOA files ?
The reference repository has a simple command line player: https://github.com/phoboslab/qoa
```bash
./qoaplay file.qoa
```

## Samples
Voice samples can be found at: https://github.com/yaph/tts-samples

## Features

* QOA de-/encoder
* **Streaming** support for both de-/encoder
* Soft realtime algorithm design (could be hard realtime if setup right)
* Dependency free

## TODO:

- [x] Flush content on close of encoding
