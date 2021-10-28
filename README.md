# chip8_emulator

- This is a simple implementation of CHIP-8 emulator in Rust. CHIP-8 is an interpreted programming language, developed by Joseph Weisbecker in the 70s. CHIP-8 emulator is a virtual machine allow CHIP-8 programs to run on.
- This CHIP-8 emulator description:
  - RAM: 4096 memory locations. The first address to load programs in is 0x200
  - Stack: 16 memory locations
  - Registers: 
    - 16 8-bit general purpose registers named V0 to VF. The VF register doubles as a flag for some instructions
    - 1 16-bit I register used as a pointer for memory access
    - 1 16-bit program counter holds the address of the next instruction should be execute
  - Timers:
    - Delay timer: intended to be used for timing the events of games
    - Sound timer: used for sound effects
  - Graphics: a 64x32 monochrome display
  - Input: 16 keys input
  - Opcode: CHIP-8 has 35 opcodes, which are all two bytes long and stored big endian

## Screenshot
### Invaders
![Invaders](https://lh3.googleusercontent.com/d/1TaVHPxEpEAwWgn01VMeZmdO6RAEmj2Qy)

### UFO
![UFO](https://lh3.googleusercontent.com/d/1xqu0Rbn-5ET8YGUfwuc8oQ3B1fx5FeOK)

## How to run it
  - By using the following command:
    ```
    cargo run roms/game_name
    ```
  With ```game_name``` is the game you chose. All the game files will be at the ```roms``` folder
