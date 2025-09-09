# 8-Bit Binary Symmetry Detector

## Overview
The 8-Bit Binary Symmetry Detector is a digital logic circuit that analyzes an 8-bit binary input and detects various types of symmetry and patterns. It provides multiple outputs indicating specific symmetrical properties of the input pattern.

## Inputs and Outputs

| Port  | Type   | Description               |
|-------|--------|---------------------------|
| IN0   | Input  | Bit 0 (LSB)               |
| IN1   | Input  | Bit 1                     |
| IN2   | Input  | Bit 2                     |
| IN3   | Input  | Bit 3                     |
| IN4   | Input  | Bit 4                     |
| IN5   | Input  | Bit 5                     |
| IN6   | Input  | Bit 6                     |
| IN7   | Input  | Bit 7 (MSB)               |
| OUT1  | Output | All Zeros Detection       |
| OUT2  | Output | All Ones Detection        |
| OUT3  | Output | Palindrome Detection      |
| OUT4  | Output | Mirror Symmetry           |
| OUT5  | Output | Even Parity Check         |
| OUT6  | Output | Odd Parity Check          |
| OUT7  | Output | Special Pattern Detection |

## Symmetry Detection Logic

| Output | Condition | Description |
|--------|-----------|-------------|
| OUT1   | IN0-IN7 = 00000000 | All bits are 0 (Null pattern) |
| OUT2   | IN0-IN7 = 11111111 | All bits are 1 (Full pattern) |
| OUT3   | IN0=IN7, IN1=IN6, IN2=IN5, IN3=IN4 | Perfect palindrome symmetry |
| OUT4   | IN0=IN7, IN1=IN6, IN2=IN5, IN3=IN4 | Mirror symmetry around center |
| OUT5   | Even number of 1's | Even parity check |
| OUT6   | Odd number of 1's  | Odd parity check |
| OUT7   | Custom pattern     | Special pattern detection |

## Truth Table Examples

| Input (Binary)   | OUT1 | OUT2 | OUT3 | OUT4 | OUT5 | OUT6 | OUT7 |
|------------------|------|------|------|------|------|------|------|
| 00000000         | 1    | 0    | 1    | 1    | 1    | 0    | 0    |
| 11111111         | 0    | 1    | 1    | 1    | 1    | 0    | 0    |
| 01100110         | 0    | 0    | 1    | 1    | 1    | 0    | 0    |
| 10011001         | 0    | 0    | 1    | 1    | 0    | 1    | 0    |
| 01010101         | 0    | 0    | 0    | 0    | 0    | 1    | 1    |
| 10101010         | 0    | 0    | 0    | 0    | 0    | 1    | 1    |

## Applications

1. **Error Detection Systems**: Identify data corruption by detecting unexpected symmetry breaks
2. **Data Transmission**: Verify integrity of transmitted binary data
3. **Cryptography**: Analyze patterns in encrypted data for security purposes
4. **Digital Signal Processing**: Detect repeating patterns in digital signals
5. **Memory Testing**: Identify faulty memory cells through pattern recognition
6. **Network Protocols**: Implement parity checking in data packets
7. **Educational Tool**: Demonstrate binary symmetry concepts in digital logic design

## Implementation Features

- **Combinational Logic**: Uses basic gates (AND, OR, NOT, XOR) for all operations
- **Parallel Processing**: All symmetry checks occur simultaneously
- **Visual Feedback**: LED indicators for each symmetry type
- **Scalable Design**: Can be extended to larger bit widths
- **Real-time Operation**: Instant detection with no clock required

## How to Use

1. Set the 8 input switches (IN0 to IN7) to desired binary values
2. Observe the output LEDs (OUT1 to OUT7) to see detected symmetries
3. Multiple outputs may activate simultaneously for patterns with multiple symmetrical properties
4. Use truth table examples to verify circuit operation

## Technical Specifications

- **Input**: 8-bit binary (0-5V logic levels)
- **Output**: 7-bit detection signals (active high)
- **Power Supply**: 5V DC
- **Technology**: CMOS/TTL compatible logic gates
- **Propagation Delay**: < 50ns typical
