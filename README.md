uvm_register_demo/
├── my_testbench_pkg.svh       // 包含所有 class 的头文件汇总
├── my_transaction.svh
├── my_reg.svh
├── my_adapter.svh
├── my_driver.svh
├── my_monitor.svh
├── my_scoreboard.svh          // ✅ 新增：包含 write() 比对逻辑
├── my_env.svh
├── my_test.svh
├── top.sv                     // Verilog 顶层模块 + run_test
└── README.md

# UVM Register Layer Verification Project

## Overview

This project demonstrates a complete UVM verification environment for a simple DUT with two 8-bit registers (r0, r1). It includes a register model, a register adapter, driver, monitor, and a scoreboard to check functional correctness.

## Components

- ✅ `my_reg_model` : Defines r0, r1 register structures.
- ✅ `my_adapter` : Converts register-level access into bus transactions.
- ✅ `my_transaction` : Encapsulates command, address, data fields.
- ✅ `my_driver` : Drives DUT pins based on transactions.
- ✅ `my_monitor` : Observes DUT signals and reconstructs transactions.
- ✅ `my_scoreboard` : Checks whether DUT behavior matches expected register operations.

## Key Features

- 🔧 UVM register-to-bus adapter connection via `reg2bus()` and `bus2reg()`
- ✅ Support for both read and write operations
- 🧠 Scoreboard automatically checks whether values written to r0/r1 match expected data
- 🧪 Ready for further extension (e.g., negative testing, reference model comparison)

## How to Run

