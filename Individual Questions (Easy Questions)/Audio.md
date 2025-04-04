# Audio to Sine Wave Converter

## Description
In embedded systems, devices like MP3 players or audio decoders often communicate using low-level protocols such as SPI (Serial Peripheral Interface). MP3 files must be converted into a stream of data suitable for transmission over SPI, and in some cases, this stream must be stored or analyzed, then converted back into a playable MP3.

You are developing a software component for an embedded system that handles MP3 playback. The system must transmit MP3 files over SPI and later reconstruct them for verification or playback.

A playable MP3 file is provided to you as input.

### Task 1: MP3 → SPI

Write a program that reads the binary data of an .mp3 file and writes it into a .spi file.
- The .spi file is a binary representation of what would be sent over SPI.
- The data must be written in fixed-size chunks (e.g., 32 bytes per “packet”).
- You can optionally include headers or markers per chunk to simulate framing.

### Task 2: SPI → MP3

Write a second program (or function) that reads the .spi file and reconstructs the original .mp3.
- The resulting .mp3 file must be playable and identical to the input MP3.
- Any headers or formatting used in the .spi file must be correctly removed or handled.

Input Format
- A playable MP3 file (input.mp3)

Output Format
- A .spi file containing the encoded transmission stream (output.spi)
- A reconstructed MP3 file (reconstructed.mp3)

### Constraints
1. You may not use external libraries for audio processing — only standard file I/O.
2. Must create two seperate programs meeting the described behaviors
3. Real-time processing capability
4. Memory efficient implementation
5. Data integrity must be preserved — the reconstructed .mp3 must match the original byte-for-byte.
6. If you are not familiar with spi and mp3 you may reasearch their datatypes and structures

## Success Criteria
- The reconstructed MP3 file (reconstructed.mp3) must be:
- Playable using any standard media player.
- Identical in size and content to the original input.mp3.
- No use of artificial intelligence or machine learning algorithms should be involved in the creation of your program