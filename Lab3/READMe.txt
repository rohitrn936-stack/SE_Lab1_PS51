Lab3 - Component Modelling & Architectural Pattern Selection
============================================================

This folder contains the Lab 3 deliverables for the Self-Service Coffee Kiosk System analysis.

Deliverables:
- componentDiagram.drawio: Editable draw.io source file for the UML component diagram
- componentDiagram.pdf: Exported PDF of the component diagram
- architectureJustification.docx: Word document with architecture justification
- architectureJustification.pdf: PDF export of the architecture justification

Components:
1. User Interface Component - Handles touchscreen interactions
2. Order Manager Component - Processes and manages orders
3. Payment Service Component - Handles credit card payment processing
4. Receipt Printer Component - Generates and prints receipts
5. Database Component - Stores menu data, pricing, and order information

Architectural Style: Layered Architecture
- Selected for clear separation of responsibilities
- Enables secure credit card payment processing
- Supports touchscreen interaction through dedicated UI layer
- Provides performance benefits through localized optimization

Interfaces (4 minimum):
- User Interface → Order Manager: orderSubmission
- Order Manager → Payment Service: paymentRequest
- Order Manager → Receipt Printer: receiptGeneration
- Order Manager → Database: dataAccess

Quality Verification:
- All five components present and correctly named
- At least four interfaces shown between components
- Provided and required interface notation using ball/socket UML conventions
- Assembly connectors connect provided interfaces to required interfaces
- Interface directions and labels are meaningful and descriptive
- Component interactions and data flow are visible and understandable

Security Advantage: The Layered Architecture isolates credit card payment data within the Payment Service layer, providing defense-in-depth protection. Sensitive card information is not exposed to the User Interface or other layers, and all payment requests flow through the Order Manager as a controlled gateway.

Performance Benefit: The Layered Architecture offers performance benefits through localized optimization. Each layer can be independently optimized - the Database layer can use connection pooling and query optimization, the Payment Service can employ caching for frequent transactions, and the Order Manager can batch operations. The overall system response time for touchscreen interactions and order fulfillment remains fast and predictable.

Two Scenario-Specific Reasons:
1. Touchscreen interaction separation: The User Interface layer handles touchscreen inputs in a dedicated layer, allowing the Order Manager to focus on processing orders without worrying about low-level hardware details.
2. Payment processing isolation: The Layered Architecture cleanly separates the Payment Service layer from the Order Manager, allowing credit card payment processing to be handled securely in its own layer.