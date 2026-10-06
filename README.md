# Hi, I'm Beck 👋

**Mathematics & Computer Science student at the University of Minnesota** (Physics minor)

I love optimizing and solving hard problems, especially ones where a system has to make good decisions fast, with no obvious rules to follow. Most of my work lives at the intersection of **machine learning** and **efficient search algorithms**, and most of it is written in **Rust**.

I'm especially interested in how these ideas carry over to real-world problems where speed and good decisions matter: quantitative finance, aerospace, and more.

📫 [beckbjella@gmail.com](mailto:beckbjella@gmail.com) · 💼 [LinkedIn](https://www.linkedin.com/in/beck-bjella-a4022b279/)

---

## 🎲 Featured: Gyges Engine

The first open-source engine for the board game Gygès, a game with no established strategy theory. I also built [gyges.app](https://gyges.app/), the only place online to play against a Gygès engine.

[**▶ Play it**](https://gyges.app/) · [Repository](https://github.com/Beck-Bjella/Gyges) · [crates.io](https://crates.io/crates/gyges)

- **Neural evaluation:** an original MLP with pair-encoded sparse inputs (similar to Stockfish's HalfKP), trained solely on self-play game outcomes. It beat my previous engine 200–1, and that engine was already unbeatable for humans.
- **Move generation:** an original backtracking resistant move generator for complex chained moves, built on precomputed path tables indexed with x86-64 `pext`. The first version, in Python, couldn't finish a 1-ply search; after a Rust rewrite and two years of optimization, it reaches 21+ ply.
- **Search:** multithreaded YBWC principal variation search with a lockless transposition table, at 300,000+ nodes/sec.
- **Runs anywhere:** compiled to WebAssembly to run client-side in the browser.

Full technical details are in the [repository](https://github.com/Beck-Bjella/Gyges).

---

## 🤖 FRC Team 2264: Robot Software
*Programming Captain (2023) · Head Captain (2024)*

- Redesigned the team's Java codebase into a **command-based architecture**, the code behind our run to the **FIRST World Championships**
- Built real-time computer vision tracking of game pieces for driver assistance
- Left a documented, modular codebase for future team members to adapt.

[FRC-2024 repository](https://github.com/Team-2264/FRC-2024)

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
