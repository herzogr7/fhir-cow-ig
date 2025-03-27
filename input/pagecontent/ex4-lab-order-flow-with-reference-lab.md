### Lab Order Workflow with involment of a Reference Lab 
### - Herpes simplex virus Ab panel - Serum triggers a Herpes simplex virus Ab.IgM -

#### Important Information
- This is a **minimal viable definition** of a possible laboratory workflow with a reference lab
- This is not implementable for now but tries to show the flow of the order and the minimal needed information
  
#### Assumptions
- Physician knows which Specimen to draw (i.e. via an Order Catalog)
- Specimen is drawn by the Physician
- It is clear which Order Filler will execute the Order
- ""ServiceRequest"" is owned by the Order Placer; changes are allowed only to be done by Placer
- ""Task"" is a shared resource of Placer and Filler and updated by both
- Order Result is reported via ""DiagnosticReport""
- ""DiagnosticReport"" is owned by the Order Filler
- Order is accepted and is fulfilled by 
  - Community Lab and
  - Reference Lab
- Lab internal flow is **out of scope**
- Lab will trigger a Herpes simplex virus Ab.IgM Reference Lab Reflex test 
- All needed data is accessible
- All needed data around the Sample is in the `Specimen` like collection information (`Procedure` collection date/time, body Site, ...)
#### Not defined
- Ownership of Specimen Resource (Ownership should/could/might change with the physical location)
- Transport of the Sample

### Example using Subscriptions with Task at Placer
<figure>
  {% include ex4-lab-order-flow-with-reference-lab.svg %}
</figure>
