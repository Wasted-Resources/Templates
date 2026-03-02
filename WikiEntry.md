# Component: [Component Name, e.g., SaveManager]

## 1. Overview
* **Origin Issue:** [Link to Issue #]
* **Architecture Issue:** [Link to Architecture #]
* **Primary Author:** @[Username]

## 2. Component Requirements
*Extract requirements directly from the issue comments.*
- [Requirement 1, e.g., Must support up to 8 save files per slot]
- [Requirement 2, e.g., Data must be AES-encrypted before writing to disk]

## 3. Implementation Details
*Reference the logic used in the script.*
- **Persistence:** Uses `Application.persistentDataPath` for cross-platform support.
- **Security:** Implements `Aes` encryption with fixed IV/Key for profile data.

## 4. API & Synchronization
*Describe how this component talks to the Node.js backend.*
- Calls `RestApi.AddSession` on new game start.
- Synchronizes statistics via `UpdateSession` during the save loop.

## 5. Deployment Notes
- This script must be attached to the `[GlobalManager]` Prefab in the Bootstrap scene.