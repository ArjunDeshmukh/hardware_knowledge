# Broadcom BCM2712 Specifications Explained

* **Quad-core Arm Cortex-A76 @ 2.4 GHz** — This is the main central processing unit (CPU), featuring four high-performance Arm Cortex-A76 cores running at 2.4 GHz to handle general computing tasks.
  * **Armv8-A ISA** — This specifies the 64-bit instruction set architecture used by the CPU, enabling it to run modern 64-bit software while retaining backward compatibility for 32-bit applications.
  * **64 kByte I and D caches** — Each CPU core has 64 KB of dedicated Level 1 instruction (I) and data (D) cache placed directly on the core for near-instant access to active code and memory.
  * **512 kB L2 per core, 2 MB shared L3** — Every core gets 512 KB of fast Level 2 cache, while all four cores share a larger 2 MB Level 3 cache to reduce delays when fetching data from main system RAM.

* **New Raspberry Pi-developed ISP** — The chip includes a custom Image Signal Processor (PiSP) designed in-house by Raspberry Pi to process raw camera feeds, color correction, and noise reduction.
  * **1 gigapixel/sec** — The camera system can process up to one billion pixels every second, allowing for multiple high-resolution, high-framerate camera streams running simultaneously.

* **Improved HVS and display pipeline** — The upgraded Hardware Video Scaler and display engine efficiently handle visual compositing, rotation, and scaling before outputting pixels to external screens.
  * **Dual 4Kp60 support** — The processor has enough display bandwidth to drive two independent monitors at 4K resolution running at a smooth 60 frames per second.

* **VideoCore V3D VII** — This is the 7th-generation VideoCore graphics processing unit (GPU) integrated into the chip, responsible for driving user interfaces and 3D graphics.
  * **~2-2.5× faster (more hardware, 960 MHz versus 500 MHz on Raspberry Pi 4)** — With extra processing hardware and a clock speed boosted from 500 MHz to 960 MHz, graphics performance is roughly double to two-and-a-half times that of the Raspberry Pi 4.
  * **OpenGL ES 3.1, Vulkan 1.3** — The GPU supports these industry-standard graphics software libraries, allowing developers to run modern 3D games and hardware-accelerated applications smoothly.

* **4Kp60 HEVC hardware decode** — The chip includes dedicated silicon designed specifically to decompress 4K H.265 (HEVC) video at 60 fps without burdening the main CPU.
  * **Other CODECs run in software** — Because fixed hardware decoders were omitted for older or alternate video formats, the CPU handles those video streams through software processing instead.
  * **H264 1080p24 decode ~10–20% of CPU** — Decoding standard 1080p H.264 movies at 24 fps using software requires relatively little CPU power, using only 10% to 20% of its total capacity.
  * **H264 1080p60 decode ~50–60% of CPU** — Playing high-framerate 1080p H.264 video at 60 fps in software takes a noticeable effort, consuming around half of the CPU's available resources.
  * **H264 1080p30 encode (from ISP) ~30–40% CPU** — Encoding 1080p H.264 video at 30 fps directly from the camera ISP in software requires approximately 30% to 40% of the CPU's processing capability.