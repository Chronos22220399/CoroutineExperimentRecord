# 阶段一：基础理论与技术储备

## Part 1：理解协程核心概念

### 🎯 目标

- 掌握 C++20 协程语法和底层机制  
- 理解 `co_await`、`co_yield`、`co_return` 的控制流程  
- 理解 `promise_type`、`coroutine_handle`、suspend 点等实现原理  

### ⏱️ 建议用时  
3～5 天

### 📚 推荐资料

- [C++ Coroutines: Understanding the Fundamentals](https://lewissbaker.github.io/2017/11/17/understanding-operator-co-await)  
- [协程的本质（知乎）](https://zhuanlan.zhihu.com/p/59178345)  
- [cppreference 协程语法](https://en.cppreference.com/w/cpp/language/coroutines)  
- （可选）YouTube：Jason Turner 协程系列

### 🧪 练习任务

- 实现一个最小的 `Task` 协程（无任何异步，仅执行 `co_return`）  
- 修改 `initial_suspend` 和 `final_suspend`，观察协程暂停与恢复  
- 使用 `coroutine_handle` 显式 resume 协程  

---

## Part 2：掌握 I/O 多路复用与异步模型

### 🎯 目标

- 理解 `select`/`poll`/`epoll`/`io_uring` 的机制与区别  
- 能用 `epoll` 编写非阻塞 Echo 服务器  
- 初步掌握 `liburing` 的使用，了解异步 I/O 模型  

### ⏱️ 建议用时  
5～7 天

### 📚 推荐资料

- [深入理解 epoll](https://blog.csdn.net/qq_26399665/article/details/115112051)  
- [liburing GitHub](https://github.com/axboe/liburing)  
- [io_uring 101 教程](https://unixism.net/loti/)  
- （可选）《Linux 高性能服务器编程》- 游双  

### 🧪 练习任务

- 写一个基于 `epoll` 的非阻塞 Echo TCP 服务器  
- 模拟多个客户端连接并测试响应情况  
- 使用 `liburing` 实现异步文件读取  

---

## Part 3：阅读协程库源码与调度器设计

### 🎯 目标

- 理解现有协程库设计结构与调度逻辑  
- 掌握 Awaiter 对象的作用与挂起/恢复机制  
- 初步形成自己协程库的设计思路  

### ⏱️ 建议用时  
4～6 天

### 📚 推荐资料

- [libco (腾讯开源协程切换库)](https://github.com/Tencent/libco)  
- [cppcoro (基于 C++20 的协程库)](https://github.com/lewissbaker/cppcoro)  
- [Boost.Asio 协程支持](https://www.boost.org/doc/libs/release/libs/asio/doc/html/index.html)

### 🧪 练习任务

- 阅读 `cppcoro` 中 `Task<T>` 的实现并做注释  
- 用流程图总结协程的创建、挂起、恢复过程  
- 草拟你自己的调度器结构设计图（可暂不实现）  

---

## 📌 建议与补充

- 每完成一个小节，建议写一篇笔记总结关键概念与代码实现思路  
- 可同步学习 CMake 与构建系统，为第二阶段打基础  
