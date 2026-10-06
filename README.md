# Hi, I'm Beck 👋

**Mathematics & Computer Science student at the University of Minnesota** (Physics minor)

I love optimizing and solving hard problems, especially ones where a system has to make good decisions fast, with no obvious rules to follow. Most of my work lives at the intersection of **machine learning** and **efficient search algorithms**, and most of it is written in **Rust**.

I'm especially interested in how these ideas carry over to real-world problems where speed and good decisions matter: quantitative finance, aerospace, and more.

📫 [beckbjella@gmail.com](mailto:beckbjella@gmail.com) · 💼 [LinkedIn](https://www.linkedin.com/in/beck-bjella-a4022b279/)

---

## 🎲 Featured: Gyges Engine

The first open-source engine for the board game Gygès, a game with no established strategy theory. I also built [gyges.app](https://gyges.app/), the only place online to play against a Gygès engine.

[**▶ Play it**](https://gyges.app/) · [Repository](https://github.com/Beck-Bjella/Gyges) · [crates.io](https://crates.io/crates/gyges)

- **Neural evaluation:** an original MLP with 5,886 sparse inputs (piece-square plus same- and cross-type piece-pair features, similar to Stockfish's HalfKP) feeding a 1,024-unit hidden layer, with the board mirrored for side to move. Trained solely on game outcomes, using about 28M positions from self-play games generated on AWS EC2, each labeled with the eventual winner. It beat my previous engine 200–1 under identical search settings, and that engine was already unbeatable for humans.
- **Move generation:** an original generator for complex chained moves that can double back on themselves. Every legal path for every square and blocker configuration is precomputed, and blockers are compressed into table indices with the x86-64 BMI2 `pext` instruction, so generation is table lookups instead of a live backtracking search. Rust generics specialize it at compile time into separate paths for move lists, move counts, and threat detection. The first version, in Python, couldn't finish a 1-ply search; after a Rust rewrite and two years of optimization, it reaches 21+ ply.
- **Search:** multithreaded YBWC principal variation search at 300,000+ nodes/sec, with iterative deepening, aspiration windows, a lockless Zobrist-hashed transposition table, and bitboard board state.
- **Runs anywhere:** compiled to WebAssembly to run client-side on my website for the game, [gyges.app](https://gyges.app/), with a software `pext` fallback since WASM has no BMI2.

Full technical details are in the [repository](https://github.com/Beck-Bjella/Gyges).

---

## 📂 More Projects

- **[GygesUI](https://github.com/Beck-Bjella/GygesUI):** desktop app for playing Gygès against the engine
- **[Browse all my repositories →](https://github.com/Beck-Bjella?tab=repositories)**

---

## 🛠️ Tech

**Languages:** Rust · Python · Java  
**ML & Data:** PyTorch · NumPy · YOLOv8  
**Infrastructure:** AWS (EC2) · WebAssembly · Git  
**Methods:** neural network training · game-tree search · computer vision · pose estimation
