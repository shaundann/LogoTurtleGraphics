# 🐢 Logo Turtle Graphics – CS Assignment

A lightweight C implementation of Logo-style turtle graphics — built from scratch for my Computer Science coursework.
Feed it simple movement commands and watch it draw crisp bitmaps pixel-by-pixel, just like the classic Logo turtle!

---

## ✨ Key Features

* **Command Parser** – Reads `forward`, `left`, `right`, `penup`, `pendown`, `repeat … [ … ]`, and custom distance / angle values.
* **Linked-List Program Representation** – Every instruction is stored as a `CmdNode` so you can traverse, query, or mutate the script with ease.
* **Raster Renderer** – Outputs a 2-D `Image` array (`SIZEX × SIZEY`) you can dump to PPM/PNG or preview in-terminal.
* **Error Handling** – Detects invalid tokens, out-of-bounds moves, and unmatched brackets before execution starts.
* **Unit Tests** – Coverage for the parser, executor, and renderer to guard against regressions.

---

## 🚀 Getting Started

```bash
# Clone the repo
git clone https://github.com/<your-handle>/logo-turtle-graphics.git
cd logo-turtle-graphics

# Build (requires a C11-compatible compiler)
make            # or: gcc -std=c11 -Wall -Wextra *.c -o turtle

# Run an example script
./turtle examples/spiral.logo output.ppm
```

### Example `.logo` file

```logo
# Draw a square spiral
repeat 36 [
    forward 10
    right 90
    forward 10
    right 90
    forward 10
    right 90
    forward 10
    right 95   ; tighten the spiral
]
```

## 🤝 Contributing

Pull requests are welcome! If you spot a bug or have a command you’d love to see, open an issue first to discuss what you’d like to change.

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.

> **Why this exists:** Writing the entire Logo pipeline myself deepened my understanding of parsing, linked-list data structures, and low-level image manipulation — and it’s surprisingly fun to watch a minimalist C program sketch art!
