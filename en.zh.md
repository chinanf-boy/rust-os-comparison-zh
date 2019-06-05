# Rust OS 比较

[Rust](https://rustlang.org)编写的操作系统的比较。

有几个用 Rust 编写的开源操作系统。其中大多数都是概念的证明。唯一更进一步的系统是**redox**。它配备了一个窗口管理器，以及基本的应用程序像[编辑器](https://github.com/redox-os/sodium)和文件管理器。

- **redox**（[存储库](https://github.com/redox-os/redox)/[主页](http://www.redox-os.org/)）
- **Tock**（[存储库](https://github.com/helena-project/tock)/[主页](http://www.tockos.org/)）
- **intermezzOS**（[存储库](https://github.com/intermezzos/kernel)/[主页](http://intermezzos.github.io/)）
- **reenix**（[存储库](https://github.com/scialex/reenix)）
- **rustboot**（[存储库](https://github.com/charliesome/rustboot)）
- **RustOS**（[存储库](https://github.com/ryanra/RustOS)）
- **QuiltOS**（[存储库](https://github.com/QuiltOS/QuiltOS)）
- **Tifflin (rust_os)**（[存储库](https://github.com/thepowersgang/rust_os)）
- **bkernel**（[存储库](https://github.com/rasendubi/bkernel)）
- **Quasar**（[存储库](https://github.com/LeoTestard/Quasar)）
- **SOS**（[存储库](https://github.com/hawkw/sos-kernel)）

| 名              | 架构              | 纯 Rust | 活跃吗? | 内核架构                         | 目标人群         | 用户空间? | 可选 GUI? | 贡献者 | 文件系统        | 许可                       |
| --------------- | ----------------- | ------- | ------- | -------------------------------- | ---------------- | --------- | --------- | ------ | --------------- | -------------------------- |
| **redox**       | x86 and x86_64    | yes     | yes     | 微内核                           | 通用目的         | yes       | yes       | 50     | [ZFS]/[RedoxFS] | MIT                        |
| **Tock**        | Cortex M          |         | yes     |                                  |                  |           | no        | 40     |                 | APL 2 / MIT                |
| **intermezzOS** | x86_64            | no      | yes     | ?                                | PoC              | no        | no        | 18     | no              | APL 2 / MIT                |
| **RustOS**      | i386              | ?       | yes     | None                             | PoC              | no        | no        | 10     | no              | APL 2 / MIT                |
| **rustboot**    | i386              | ?       | no      | None                             | PoC              | no        | no        | 8      | no              | MIT                        |
| **bkernel**     | ARM               | yes     | yes     | ?                                | Embedded devices | no        | no        | 4      | ?               | GPL with linking exception |
| **SOS**         | x86_64            | yes     | yes     | 微内核                           | PoC              | no        | no        | 3      | ?               | MIT                        |
| **reenix**      | [Brown's CS167/9] | no      | no      | 整体(Monolithic) (current state) | PoC              | no        | no        | 3      | ?               | [unknown]                  |
| **Quasar**      | x86_64            | ?       | no      | ?                                | ?                | no        | no        | 2      | ?               | ?                          |
| **Tifflin**     | x86_64/amd64      | almost  | yes     | 整体(Monolithic)                 | ?                | ?         | yes       | 1      | ISO9660         | 2-Clause-BSD               |

另外值得注意的是：[Robigalia](https://github.com/robigalia/sel4-sys)，一个 sel4 用户空间，用 Rust 编写。

[brown's cs167/9]: http://cs.brown.edu/courses/cs167/
[zfs]: https://github.com/redox-os/zfs
[redoxfs]: https://github.com/redox-os/redoxfs
[unknown]: https://github.com/scialex/reenix/issues/1

## 博文和论文

\-[为 Micro:bit 编写第二个 Rust 视频游戏](https://hackernoon.com/writing-the-second-video-game-for-the-micro-bit-in-rust-3cd8b5ab22d3)

- Tock 周会谈

  - [5](http://www.tockos.org/blog/2016/talking-tock-5/)，
  - [4](http://www.tockos.org/blog/2016/talking-tock-4/)，
  - [3](http://www.tockos.org/blog/2016/talking-tock-3/)，
  - [2](http://www.tockos.org/blog/2016/talking-tock-2/)，
  - [1](http://www.tockos.org/blog/2016/talking-tock-1/)

- [FreeRTOS 符合 Rust](http://www.hashmismatch.net/freertos-meets-rust/)
- [务实的，裸机 Rust](http://www.hashmismatch.net/pragmatic-bare-metal-rust/)
- 本周 intermezzOS：

  - [1](https://intermezzos.github.io/blog/articles/twii1/)，
  - [2](https://intermezzos.github.io/blog/articles/twii2/)，
  - [3](https://intermezzos.github.io/blog/articles/twii3/)

- [Rust 编写操作系统](http://os.phil-opp.com/)

  - [从异常回来](http://os.phil-opp.com/returning-from-exceptions.html)
  - [分配帧](http://os.phil-opp.com/allocating-frames.html)
  - [打印到屏幕](http://os.phil-opp.com/printing-to-screen.html)
  - [设置 Rust](http://os.phil-opp.com/setup-rust.html)
  - [进入长模式](http://os.phil-opp.com/entering-longmode.html)
  - [一个最小的 x86 内核](http://blog.phil-opp.com/rust-os/multiboot-kernel.html)
  - [重新映射内核](http://os.phil-opp.com/remap-the-kernel.html)
  - [内核堆](http://os.phil-opp.com/kernel-heap.html)

- [本周在 Redox1](http://www.redox-os.org/news/this-week-in-redox-1/) / [ Redox 新闻](http://www.redox-os.org/news/)
- [ Redox 是认真的](http://dictator.redox-os.org/index.php?controller=post&action=view&id_post=17)
- [Reenix：Rust 实现类 Unix 操作系统](https://scialex.github.io/reenix.pdf)（PDF）
- [Rust 构建操作系统的经验](https://mostlytyped.com/posts/experiences-building-an-os-in-ru)
- [以极小的步骤，Rust 编写 OS（步骤 1-5）](http://jvns.ca/blog/2014/03/12/the-rust-os-story/)
- [我的 Rust OS 永远不会完成（这是成功的！）](http://jvns.ca/blog/2014/03/21/my-rust-os-will-never-be-finished/)
- [所有权是 Theft：经验 Rust 构建嵌入式操作系统](http://amitlevy.com/papers/tock-plos2015.pdf)（PDF）
- [将 Rust 用于本科操作系统课程](http://rust-class.org/0/pages/using-rust-for-an-undergraduate-os-course.html)
- [在 Rumprun unikernel 上运行 Rust](https://gandro.github.io/2015/09/27/rust-on-rumprun/)
- [制作爆米花：将磁盘添加到 Rust Rumprun Unikernel](https://polyfractal.com/post/adding-a-disk-to-a-rust-rumprun-unikernel/)
- [bkernel：Rust 操作系统](http://www.alexeyshmalko.com/2015/bkernel-a-rust-operating-system/)
- [（x86_64）为什么默认情况下，启用红色区域等平台功能？](https://internals.rust-lang.org/t/x86-64-why-are-platform-features-such-as-the-red-zone-enabled-by-default/)
- [操作系统开发维基](https://github.com/rust-lang/rust-wiki-backup/blob/master/Operating-system-development.md)
- [在 seL4 之上，创建一个安全的 POSIX 兼容用户空间](https://robigalia.org/)
- [在 Rust geschrieben 的 Betriebssystem Redox](http://www.pro-linux.de/news/1/23383/betriebssystem-redox-in-rust-geschrieben.html)（德语）

### 嵌入式系统

- [更安全的微控制器，几乎就在这里](http://dylanmckay.io/blog/rust/avr/llvm/2017/02/09/safer-microcontrollers-almost-here.html)
- [探索 Rust 中的 ARM 内联汇编](http://embed.rs/articles/2016/arm-inline-assembly-rust/)
- 裸机 Rust
  - [3：配置 PIC，以正确处理中断](http://www.randomhacks.net/2015/11/16/bare-metal-rust-configure-your-pic-interrupts/)
  - [2：重新定位你的编译器，这样中断不是邪恶的](http://www.randomhacks.net/2015/11/11/bare-metal-rust-custom-target-kernel-space/)
  - [1：底层 CPU I/O 端口](http://www.randomhacks.net/2015/11/09/bare-metal-rust-cpu-port-io/)
- [在 ARM 微控制器上，Rust 裸机](http://antoinealb.net/programming/2015/05/01/rust-on-arm-microcontroller.html)
- [在 Beaglebone Black 上，Rust 写的，一个闪烁 LED](http://theotherandygrove.com/blinking-an-led-with-rust-on-a-beaglebone-black/)
- [Zinc 目标被重新定义和扩展](http://zinc.rs/blog/#/2014/07/14/zinc-goals/)
- 在 Arduino Uno 上的 Rust
  - [第 1 部分](http://jakegoulding.com/blog/2016/01/02/rust-on-an-arduino-uno/)
  - [第 2 部分](http://jakegoulding.com/blog/2016/01/17/rust-on-an-arduino-uno-part-2/)
  - [第 3 部分](http://jakegoulding.com/blog/2016/01/24/rust-on-an-arduino-uno-part-3/)
  - [第 4 部分](http://jakegoulding.com/blog/2016/05/12/rust-on-an-arduino-uno-part-4/)
- [Arduino Due 的锈](http://de.slideshare.net/kellogh/glue-con14)
- <http://embedded.hannobraun.de/>
- [Raspberry Pi 裸机 Rust 编程](https://blog.thiago.me/raspberry-pi-bare-metal-programming-with-rust/)
- [在 BBC micro:bit 微控制器上，运行 Rust 代码](https://github.com/SimonSapin/rust-on-bbc-microbit)
