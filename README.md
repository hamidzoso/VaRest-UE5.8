# VaRest for Unreal Engine 5.8 (Unofficial Port)

This is an unofficial update and port of the popular **VaRest** plugin, updated to be fully compatible with **Unreal Engine 5.8**. 

Since the original repository has not yet been updated for the latest engine structural changes, this fork resolves several compilation and runtime issues introduced by the UE 5.8 API updates.

## 🛠️ What's Changed & Fixed

This version fixes multiple C++ compilation errors related to deprecated APIs and structural refactoring in Unreal Engine 5.8:

* **TSharedString Fixes:** Updated `UE::TSharedString` implementations to correctly resolve compilation crashes (C2440/C2039) by adapting to the updated underlying string and type safety constraints.
* **Array Memory Management:** Fixed calls to `TArray::Pop` and `RemoveAt` by replacing deprecated boolean parameters with the new `EAllowShrinking` enum constraints required by UE 5.8.
* **FJsonObject / TMap Interoperability:** Refactored object fields and map structures to align with the stricter type constraints and reference handling in the latest engine codebase.

## 🚀 Installation

1. Create a `Plugins` folder in your Unreal Engine 5.8 project root directory (if it doesn't exist yet).
2. Clone or download this repository into that folder:
   ```bash
   YourProject/Plugins/VaRest/
