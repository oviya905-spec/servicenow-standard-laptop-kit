# servicenow-standard-laptop-kit - dev443146 - Oviya S

> ServiceNow PDI Instance: dev443146.service-now.com
> Catalog Item: Standard Laptop
> Owner: Oviya S | 2026

## Assignment Objective
Automate Standard Laptop request fulfillment using Flow Designer with auto Catalog Task creation.

## CURRENT STATUS - PROVEN & WORKING

### Latest Test: RITM0010005 - SUCCESS
- Instance: dev443146.service-now.com
- Requested Item: RITM0010005
- Catalog Item: Standard Laptop
- Request: REQ0010005
- State: Open | Stage: Order Fulfillment
- Impact: 3 - Low

### Auto Task Creation - WORKING
- Catalog Tasks (1): SCTASK0010002
- Assignment Group: Procurement
- Request Item Link: RITM0010005 -> SCTASK0010002
- Flow: Oviya Standard Laptop Onboarding - ACTIVE

## Flow Designer Configuration

Flow Name: Oviya Standard Laptop Onboarding

Trigger:
- Table: Service Catalog Requested Item [sc_req_item]
- Condition: Item = Standard Laptop
- When: Record Created

Actions:
1. Log - Start fulfillment for Standard Laptop
2. Create Catalog Task
   - Name: Procurement - Standard Laptop
   - Assignment Group: Procurement
   - Request Item: Trigger -> Requested Item Record

## How to Reproduce

1. Open Service Portal: https://dev443146.service-now.com/sp
2. Search: "Standard Laptop" > Open Catalog Item
3. Add to Cart > Order Now
4. Note REQ and RITM number (REQ0010005 / RITM0010005)
5. Open RITM > Scroll to Related Links > Catalog Tasks
6. Verify SCTASK auto-created

## Screenshots Proof

- RITM0010005 - Requested Item page
- SCTASK0010002 - Procurement group task
- Flow Context - Successful execution

## Links

- PDI: https://dev443146.service-now.com
- GitHub: https://github.com/oviya905-spec/servicenow-standard-laptop-kit

Status: COMPLETE & VERIFIED
Last Updated: 2026-10-22
