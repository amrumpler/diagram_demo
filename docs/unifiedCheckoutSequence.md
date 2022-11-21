#Unified Checkout Sequence
```mermaid
sequenceDiagram
	autonumber
	title Unified checkout flow

	actor RA
	participant CamperHub Cart Service
	participant CamperHub PMS Switch
	participant CamperHub Payment Adapter
	participant Kafka

	RA->>+CamperHub Cart Service: POST /cart (anonymous user creates cart)
	CamperHub Cart Service-->>-RA: 201 Created (URI of cart on location)
```