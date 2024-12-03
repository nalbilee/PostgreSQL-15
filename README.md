
# PostgreSQL 15 Test Assignment

This repository contains the results of the PostgreSQL 15 compilation and testing assignment.

## Contents
1. **README.md** - This file with a detailed report of the task.
2. **Logs** - Folder containing logs of PostgreSQL tests and errors.
3. **Configurations** - Folder with modified configuration files.

---

## Tasks Completed

### 1. Compilation of PostgreSQL 15 on Linux
- Successfully compiled PostgreSQL 15 from source as per the official guide.
- Verified server initialization and startup.

### 2. Running Regression Tests
- All default regression tests executed using `make check`.
- Results stored in `Logs/initial_test_results.log`.

### 3. Failing a Test by Configuration Change
- Modified `postgresql.conf` to force a connection limit issue:
  ```
  max_connections = 2
  shared_buffers = 64MB
  ```
- Test failure logged in `Logs/failed_test_results.log`.

### 4. Diagnosing the Problem
- Identified connection limits as the root cause of the failure.
- Logged diagnosis in `Logs/diagnostics.log`.

### 5. Server Crash (Advanced Task)
- Induced server crash by manipulating `pg_class` system table.
- Server logs captured in `Logs/crash.log`.

---

## Usage
1. Open logs in the `Logs` folder for details.
2. Configurations can be found in the `Configurations` folder.

---

## License
This work is released under the MIT License.
