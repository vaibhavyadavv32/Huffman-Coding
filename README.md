# Huffman Compression & Decompression 🔐📦

A complete C++ implementation of **Huffman Coding** — a lossless text compression algorithm that reduces file size by encoding characters based on frequency.

---

## 📂 Features

- ✅ Encode text files using Huffman Coding  
- ✅ Decode compressed `.huff` files back to original  
- ✅ Bit-level binary encoding using fixed 128-bit headers  
- ✅ Manual file handling (`fstream`) with binary I/O  
- ✅ Priority queue–based tree construction  
- ✅ Minimal external dependencies (only STL)

---

## 🧠 How It Works

Huffman Coding compresses data by assigning shorter binary codes to more frequent characters. This implementation:

1. Reads input file and builds a frequency table
2. Constructs a binary Huffman tree
3. Encodes characters using binary codes
4. Writes metadata + encoded binary to output
5. On decoding: reconstructs the tree and restores text

---

## 🛠️ Build Instructions

### 🔧 Prerequisites

- C++17 compatible compiler (`g++`, `clang++`, etc.)

### 🧱 Compile

```bash
g++ -std=c++17 huffman.cpp huffman-encoding.cpp -o huffmanEncoding
g++ -std=c++17 huffman.cpp huffman-decoding.cpp -o huffmanDecoding

// compression
huffmanEncoding in.txt out.huff

// decompression
huffmanDecoding out.huff in_copy.txt
