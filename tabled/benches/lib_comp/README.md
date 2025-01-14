# Benchmark's result

|                          | cli_table      | comfy_table  | tabled             | tabled_color       | tabled_par        | term_table    |
|--------------------------|----------------|--------------|--------------------|--------------------|-------------------|---------------|
| test_const_table/1       | 2.8±0.02µs     | 5.3±0.07µs   | 1974.4±100.72ns    | **1727.3±24.80ns** | 20.2±0.49µs       | 4.7±0.04µs    |
| test_const_table/8       | 53.8±0.76µs    | 59.0±2.65µs  | **26.3±0.27µs**    | 27.8±0.70µs        | 79.6±4.62µs       | 101.9±0.86µs  |
| test_const_table/32      | 662.5±8.78µs   | 865.4±4.49µs | **395.8±2.06µs**   | 398.6±2.96µs       | 450.6±21.39µs     | 1281.5±8.86µs |
| test_const_table/128     | 9.6±0.11ms     | 11.9±0.09ms  | **5.4±0.04ms**     | 6.1±0.04ms         | 5.5±0.28ms        | 18.0±0.14ms   |
| test_const_table/512     | 172.0±1.44ms   | 195.5±1.27ms | 91.3±2.43ms        | 90.7±2.05ms        | **80.7±2.70ms**   | 290.6±1.49ms  |
| test_dynamic_table/1     | 2.6±0.03µs     | 4.8±0.06µs   | 1470.9±22.17ns     | **1453.8±28.48ns** | 19.3±0.53µs       | 3.0±0.02µs    |
| test_dynamic_table/8     | 46.6±0.94µs    | 50.0±0.49µs  | 22.3±0.24µs        | **21.7±0.29µs**    | 71.9±3.84µs       | 68.0±0.75µs   |
| test_dynamic_table/32    | 547.3±4.25µs   | 784.6±7.05µs | 338.5±3.10µs       | **336.8±5.03µs**   | 401.4±21.20µs     | 984.3±9.86µs  |
| test_dynamic_table/128   | 7.5±0.07ms     | 11.7±0.09ms  | **4.6±0.05ms**     | **4.6±0.05ms**     | 4.8±0.35ms        | 14.8±0.12ms   |
| test_dynamic_table/512   | 138.3±1.32ms   | 172.9±1.40ms | 79.8±2.25ms        | 85.6±2.14ms        | **70.3±3.30ms**   | 246.3±1.33ms  |
| test_empty_table/1       | 1607.7±16.72ns | 5.2±0.06µs   | **1378.8±20.19ns** | 1408.2±11.60ns     | 19.7±1.09µs       | 2.3±0.02µs    |
| test_empty_table/8       | 24.1±0.66µs    | 50.7±0.34µs  | 21.2±0.15µs        | **18.7±0.17µs**    | 66.6±4.17µs       | 46.2±0.51µs   |
| test_empty_table/32      | 291.0±3.47µs   | 684.9±6.03µs | **243.9±1.44µs**   | 244.0±1.50µs       | 323.0±31.64µs     | 617.8±6.25µs  |
| test_empty_table/128     | 3.8±0.04ms     | 10.1±0.17ms  | **3.7±0.03ms**     | **3.7±0.03ms**     | 4.0±0.27ms        | 9.1±0.06ms    |
| test_empty_table/512     | 70.1±1.01ms    | 184.0±1.35ms | 71.4±1.87ms        | 70.5±1.85ms        | **57.2±2.55ms**   | 157.5±1.12ms  |
| test_multiline_table/1   | 8.0±0.28µs     | 11.7±0.11µs  | **5.4±0.22µs**     | **5.4±0.03µs**     | 29.5±0.70µs       | 10.8±0.24µs   |
| test_multiline_table/8   | 181.8±3.24µs   | 234.6±4.86µs | 133.7±12.06µs      | **127.8±1.51µs**   | 194.4±14.10µs     | 356.9±3.38µs  |
| test_multiline_table/32  | 2.1±0.02ms     | 3.1±0.03ms   | **1777.7±12.99µs** | 1849.3±17.30µs     | 1865.5±74.60µs    | 4.9±0.07ms    |
| test_multiline_table/128 | 36.7±0.39ms    | 52.6±0.53ms  | **28.3±0.18ms**    | **28.3±0.18ms**    | 29.1±1.86ms       | 65.2±0.49ms   |
| test_multiline_table/512 | 550.1±2.67ms   | 774.2±4.13ms | 501.1±4.18ms       | 496.1±2.68ms       | **450.9±21.15ms** | 1061.6±2.10ms |

## Table Generation

You can generate the table by this command (it relays on `critcmp`).

```bash
cargo run --manifest-path=readme/Cargo.toml
```

#### System

```
Kernel: 5.18.9-arch1-1 
CPU: 11th Gen Intel i7-11850H (16) @ 4.800GHz
```
