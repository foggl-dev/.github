# Foggl

Foggl is a feature toggling tool designed to simplify software delivery pipelines by allowing dynamic control over application features without the need for code redeployment.

## Overview

Foggl consists of two main components: an admin client and a developer client. The admin client enables users to create feature toggles called "foggls" with switch states (on/off) or value states. These foggls can be dynamically adjusted without modifying code, allowing real-time changes to application behavior.

The developer client, available as a library/package in multiple programming languages, allows developers to integrate Foggl into their codebase. This integration facilitates the retrieval of foggl states/values based on authenticated permissions, enabling conditional execution of code blocks.

## Key Features

- **Dynamic Control:** Modify feature states/values in real time without redeploying code.
- **Admin Client:** Create and manage feature toggles via an intuitive interface.
- **Developer Client:** Integrate Foggl into applications using libraries/packages in various languages.
- **Authentication:** Secure access control for admin and developer clients.
- **Language-Agnostic:** Supports integration with multiple programming languages.
- **Scalability:** Capable of handling numerous foggls across different applications.

## Usage

### Admin Client

1. **Create an Account:** Sign up and log in to access the admin dashboard.
2. **Create Foggls:** Define feature toggles and set their states or values.
3. **Manage Foggls:** Modify, activate, or deactivate foggls as needed.

### Developer Client (Example - Python) -- Proof-of-concept

1. **Initialize Foggl:** Authenticate the client using CLIENT_AUTH token.
2. **Retrieve Foggl State:** Get the state or value of a foggl in your code.
3. **Conditional Execution:** Execute code based on the retrieved foggl state/value.

```python
import foggl

foggl.initialize(CLIENT_AUTH)  # Authenticate the client

foggl_state = foggl.get_state("fogglThirtyPercentOff")

if foggl_state:
    # Code block based on foggl state
    pass
else:
    # Alternate code block based on foggl state
    pass
```
