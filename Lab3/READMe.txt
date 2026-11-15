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