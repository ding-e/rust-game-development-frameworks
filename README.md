<h1 align="center">Libraries and frameworks for <br>Game Development in Rust</h1>

<p align="center">
  <img src="./community-icon.png">
</p>

<h2 align="center">Join the <a href="https://discord.gg/yNtPTb2"><u>Game Development in Rust</u></a> Discord server</h2>

This curated list is from the **Game Development in Rust** Discord server and prioritizes libraries and frameworks that have examples and are ready or almost ready for production.

For a longer list of libraries and frameworks, see [Are We Game Yet?](https://arewegameyet.rs).

The ⭐ emoji means that the framework is excellent for one of the reasons:

- Has many followers and maintainers.
- Might have few followers and maintainers, but is in excellent quality and passed the test of time.
- Uses modern standards (compared to peers).

## Rust basics

- [Rust book](https://doc.rust-lang.org/book/).
- [Standard library - Comprehensive guide to the Rust standard library APIs](https://doc.rust-lang.org/std/index.html).
- [Edition guide - Guide to the Rust editions](https://doc.rust-lang.org/edition-guide/index.html).
- [Cargo book - A book on Rust’s package manager and build system](https://doc.rust-lang.org/cargo/index.html).
- [Rustdoc book - Learn how to make awesome documentation for your crate](https://doc.rust-lang.org/rustdoc/index.html).
- [Rustc book - Familiarize yourself with the knobs available in the Rust compiler](https://doc.rust-lang.org/rustc/index.html).
- [Compiler error index - In-depth explanations of the errors you may see from the Rust compiler](https://doc.rust-lang.org/error-index.html).

## Resources to understand ECS (Entity Component System) and DOD (Data-Oriented Design)

ECS/DOD is quite a big deal in Rust. Here are some resources to understand the basics:

- [Understanding data-oriented design for entity component systems - Unity at GDC 2019](https://www.youtube.com/watch?v=0_Byw9UMn9g).
- [CppCon 2018: Stoyan Nikolov “OOP Is Dead, Long Live Data-oriented Design”](https://www.youtube.com/watch?v=yy8jQgmhbAU) - Harsh title (ECS/DOD is not a silver bullet for every problem), but useful regardless.
- [RustConf 2018 - Closing Keynote - Using Rust For Game Development by Catherine West](https://www.youtube.com/watch?v=aKLntZcp27M) - A classic presentation already - Catherine West gives several examples, explain the problems with them, and shows the alternatives.
- ["Data-Oriented Design" web book by Richard Fabian](https://dataorienteddesign.com/dodbook).

## Productivity tools for game development

- [Blender](https://www.blender.org) for 3D modeling.
- [Krita](https://krita.org/en) for 2D image creation.

## Game engines

### 2D + 3D

Recommended if you are going to work with 3D graphics, however, API changes still might happen in future releases.

- [bevy](https://bevyengine.org) Refreshingly simple data-driven game engine.
- [rg3d](https://docs.rs/rg3d) Feature-rich, production-ready, general purpose 2D/3D game engine written in Rust with a scene editor.

### 2D

Recommended if you are going to work strictly with 2D graphics.

- [emerald](https://docs.rs/emerald)
- [macroquad](https://docs.rs/macroquad)
- [ggez](https://docs.rs/ggez)
- [tetra](https://docs.rs/tetra)
- [oxygengine](https://docs.rs/oxygengine)

## Graphics-only

- ⭐ [wgpu](https://docs.rs/wgpu) Cross-platform, safe, pure-rust graphics api (Vulkan, Metal, D3D12, D3D11, OpenGLES, WebGPU).
  - [WebGPU specification here](https://www.w3.org/TR/webgpu).
  - [Tutorial here](https://sotrh.github.io/learn-wgpu).
- ⭐ [ash](https://docs.rs/ash) Low-level bindings to Vulkan.
- ⭐ [lyon](https://docs.rs/lyon) GPU-based 2D vector rendering. Built on top of `wgpu`.
- [rend3](https://docs.rs/rend3) Easy to use, customizable, efficient 3D renderer library. Built on top of `wgpu`.
- [luminance](https://docs.rs/luminance) High level. Built on top of OpenGL.
- [miniquad](https://docs.rs/miniquad) High-level. Focus on portability. Built on top of OpenGL, GLES 3 and WebGl1.
- [glium](https://docs.rs/glium) Intermediate-level. Safer wrapper for OpenGL 3+.
- [golem](https://docs.rs/golem) Intermediate-level. Higher level wrapper built on glow.
- [vulkano](https://docs.rs/vulkano) Intermediate-level. Safer wrapper for Vulkan.
- [glow](https://docs.rs/glow) Low-level. Safer wrapper for OpenGL and WebGL.
- [erupt](https://docs.rs/erupt) Low-level bindings to Vulkan.
- ⭐ [gl46](https://docs.rs/gl46) Low-level. Wrapper for OpenGL 4.6 (generated by Phosphorus).
- ⭐ [gl33](https://docs.rs/gl33) Low-level. Wrapper for OpenGL 3.3 (generated by Phosphorus).
- [sierra](https://docs.rs/sierra) Low-level control and high-level features. Built on top of `erupt`.

I believe it is fair to say that if you use libraries built on top of WGPU, you will get wider support on modern platforms (Linux, Windows, MacOS, Android and iOS).

## Window creation and OS integration

- ⭐ [winit](https://docs.rs/winit) Rusty windowing framework. The *de facto* standard in the Rust community.
- [glfw](https://docs.rs/glfw) Rust wrapper for the C GLFW3 library.
- [fermium](https://docs.rs/fermium) Rust wrapper for the C SDL2 library. Contains more than window creation features.
- [sdl2](https://docs.rs/sdl2) Rust wrapper for the C SDL2 library. Contains more than window creation features.

## Frameworks for ECS

- ⭐ [hecs](https://docs.rs/hecs) Archetype-based.
- ⭐ [yaks](https://docs.rs/yaks) Add multi-threading to `hecs`.
- [legion](https://docs.rs/legion) Archetype-based.
- [shipyard](https://docs.rs/shipyard) Sparse-based.
- [specs](https://docs.rs/specs) Bitset-based.

See [this repository](https://github.com/SanderMertens/ecs-faq#what-are-the-different-ways-to-implement-an-ecs) for information on the different types of ECS (archetype, sparse, bitset).

## Frameworks for physics and linear math (for 2D and 3D programming)

- ⭐ [glam](https://docs.rs/glam)
- ⭐ [rapier2d](https://docs.rs/rapier2d) / [rapier3d](https://docs.rs/rapier3d) New 2D/3D physics framework from the creator of `nphysics2D`/`nphysics3D`. [2D demo](https://rapier.rs/demos2d/index.html) and [3D demo](https://rapier.rs/demos3d/index.html).
- [nphysics2d](https://docs.rs/nphysics2d) / [nphysics3d](https://docs.rs/nphysics3d) 2D/3D physics.
- [cgmath](https://docs.rs/cgmath)
- [nalgebra](https://docs.rs/nalgebra)
- [ultraviolet](https://docs.rs/ultraviolet)
- [vek](https://docs.rs/vek)

## Graphical user interface (GUI)

- ⭐ [egui](https://docs.rs/egui/) Pure Rust cross-platform library. Many renderers already have an integration with `Egui`.
- ⭐ [iced](https://docs.rs/iced/) Pure Rust cross-platform library.
- [imgui](https://docs.rs/imgui/) Bindings in Rust for the Dear ImGui C++ library.

## Font (parser and/or rasterizer)

- [fontdue](https://docs.rs/fontdue)
- [swash](https://github.com/dfrg/swash)
- [rustybuzz](https://docs.rs/rustybuzz) Complete harfbuzz shaping algorithm port to Rust.
- [ttf-parser](https://docs.rs/ttf-parser) High-level, safe, zero-allocation TrueType font parser.

## Space partitioning 

- [rstar](https://docs.rs/crate/rstar/) N-dimensional [r*-tree](https://en.wikipedia.org/wiki/R*_tree) implementation
- [bvh](https://docs.rs/crate/bvh/) Bounding Volume Hierarchy, built on top of [nalgebra](https://www.nalgebra.org/).
- [kdtree](https://docs.rs/crate/kdtree/) K-dimensional tree in Rust for fast geospatial indexing and nearest neighbors lookup.
- [ncollide 2D](https://docs.rs/crate/ncollide2d/) Bounding Volume Tree implementation [(2d documentation)](https://www.ncollide.org/rustdoc/ncollide2d/partitioning/struct.BVT.html).
- [ncollide 3D](https://docs.rs/crate/ncollide3d/) Bounding Volume Tree implementation [(3d documentation)](https://www.ncollide.org/rustdoc/ncollide3d/partitioning/struct.BVT.html).
- [spade](https://docs.rs/crate/spade/) Implements  [r*-tree](https://en.wikipedia.org/wiki/R*_tree) and [delaunay triangulation](https://en.wikipedia.org/wiki/Delaunay_triangulation).
- [flat_spatial](https://docs.rs/crate/flat_spatial/) Simple flat structures such as a grid/hashmap of cells.
- [acacia](https://docs.rs/crate/acacia/)  Generic over the dimension of the partitioned space and thus supports binary trees, quadtrees, octrees, etc.

## Network

- ⭐ [tokio](https://docs.rs/tokio) Asynchronous TCP and UDP sockets.
- ⭐ [quinn](https://docs.rs/quinn) QUIC transport protocol implementation. Built on top of `tokio`.

## Audio

- ⭐ [oddio](https://docs.rs/oddio) Built on top of `cpal`.
- ⭐ [kira](https://docs.rs/kira) Built on top of `cpal`.
- ⭐ [rodio](https://docs.rs/rodio) Built on top of `cpal`.
- ⭐ [cpal](https://docs.rs/cpal) Low-level cross-platform library for audio input and output.
- [alto](https://docs.rs/alto) Wrapper for OpenAL.
- [openal](https://docs.rs/openal) Wrapper for OpenAL.

## Serialization-Deserialization

- ⭐ [serde](https://docs.rs/serde) Serialize and deserialize data structures efficiently and generically.
- ⭐ [serde-json](https://crates.io/crates/serde_json) Serialize and deserialize for **JSON format**. Built on top of `serde`.
- ⭐ [bincode](https://crates.io/crates/bincode) Serialize and deserialize for **binary format**. Built on top of `serde`.

## Other utilities

- ⭐ [image](https://docs.rs/image) Image encoding and decoding for many image formats.
- ⭐ [rayon](https://docs.rs/rayon) Introduce parallelism into existing code and guarantees data-race free executions.
- ⭐ [palette](https://docs.rs/palette) Linear color calculations.
- [pathfinding](https://docs.rs/pathfinding) Multiple implementations of path-finding algorithms.
- [salva2d](https://docs.rs/salva2d) / [salva3d](https://docs.rs/salva3d) Particle-based fluid dynamics.
- [collider](https://docs.rs/collider) Continuous 2D collision detection.
