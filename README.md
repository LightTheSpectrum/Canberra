# Canberra
Functional Design Document: Google Transit Wallet Ecosystem
Overview
This document outlines the functional design of the Google Transit Wallet ecosystem based on the provided diagram. The system integrates multiple components to manage digital transit cards and physical cards, enabling seamless transit payment and account management.

System Components
1. Android Phone
Transit App:

Acts as the user interface for managing transit cards.

Integrates with the MIFARE2GO (M2G) SDK to facilitate encrypted transit card transactions.

Google Wallet:

Provides a user-visible interface for digital transit card management.

2. Google Server
Functionality:

Interfaces with M2G for encrypted transit card operations.

No direct access; interactions occur through the M2G cloud platform and client SDK.

3. NXP MIFARE2GO (M2G)
Core Services:

Lifecycle management of MIFARE digital transit cards.

APIs for onboarding services and core functionalities.

Integration Points:

APIs connect with Google Server and Reseller systems for card management.

4. Transit SI (System Integrator)
Responsibilities:

Manages lifecycle operations of physical transit cards and accounts.

Builds and operates backend systems for transit infrastructure, including reader devices.

Payment Processor Integration:

Facilitates payment transactions between users and transit systems.

5. Reseller (G+D)
Phase 1: Offline Management
Provides digital card payloads and metadata to NXP.

Enables offline digital card purchases.

Phase 2: API Integration
Develops API integrations with M2G platform and NEC backend.

Wraps SDK of M2G client SDK for Transit App providers (e.g., Skedgo).

Interfaces with NEC for reader changes, digital card payloads, and metadata updates.

Offers potential key management services for digital cards.

Workflow Description
User Interaction
Users access their transit cards via the Android phone's Transit App or Google Wallet interface.

The Transit App communicates with the MIFARE2GO platform via Google Server to manage encrypted digital card transactions.

Backend Operations
NXP MIFARE2GO handles lifecycle management of digital cards using its APIs.

Transit SI ensures physical card lifecycle management and maintains backend infrastructure for transit readers.

Reseller Involvement
In Phase 1, Resellers provide offline support by delivering card payloads to NXP.

In Phase 2, Resellers integrate APIs to facilitate real-time interactions between NEC backend, reader infrastructure, and digital card services.

API Interactions
Component	API Purpose
Google Server	Interface with MIFARE2GO for encrypted card operations
NXP MIFARE2GO	Onboarding services, core functionalities, lifecycle management
Transit SI	Backend system APIs for account and physical card lifecycle management
Reseller	Integration with NEC backend and reader updates; SDK wrapping
Key Features
Encrypted Digital Card Management: Ensures secure transactions via MIFARE technology.

Lifecycle Management: Supports both physical and digital card lifecycles through dedicated systems.

API Connectivity: Facilitates seamless integration between Google Server, NXP MIFARE2GO, Transit SI, and Resellers.

User-Friendly Interface: Provides a visible UI through Android apps for easy access to transit services.

Future Considerations
Expansion of reseller roles to include advanced key management services.

Enhanced integration between NEC backend systems and Transit SI infrastructure.

Potential development of additional APIs for improved scalability across regions.

This functional design document provides a comprehensive view of the Google Transit Wallet ecosystem based on the attached diagram, detailing components, workflows, API interactions, and future considerations.


